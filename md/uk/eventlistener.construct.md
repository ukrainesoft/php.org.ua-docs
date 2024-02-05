---
navigation:
  - class.eventlistener.md: « EventListener
  - eventlistener.disable.md: 'EventListener::disable »'
  - index.md: PHP Manual
  - class.eventlistener.md: EventListener
title: 'EventListener::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventListener::\_\_construct

(PECL event >= 1.2.6-beta)

EventListener::\_\_construct — Створює нового слухача з'єднання, пов'язаного з основою події

### Опис

```methodsynopsis
public
   EventListener::__construct(    
    EventBase
     $base
   ,    
    callable
     $cb
   ,    
    mixed
     $data
   ,    
    int
     $flags
   ,    
    int
     $backlog
   ,    
    mixed
     $target
   )
```

Створює нового слухача з'єднання, пов'язаного з основою події.

### Список параметрів

`base`

Основа події.

`cb`

Callback-функція ([callable](language.types.callable.md)), яка буде викликана при отриманні з'єднання.

`data`

Дані користувача, які будуть передаватися в параметр `cb`

`flags`

Битовая маска из семейства констант`EventListener::OPT_*`. Докладніше про це розказано у розділі «[Константи EventListener](class.eventlistener.md#eventlistener.constants)».

`backlog`

Керує максимальною кількістю очікуваних підключень, яким мережевий стек повинен дозволити в будь-який час очікувати в стані «не прийнято». Додаткову інформацію дивіться у документації щодо функції `listen` поточної системи. Якщо значення параметра `backlog` негативно, модуль Libevent сам спробує вибрати найкраще значення для параметра `backlog`. Якщо значення дорівнює нулю, модуль Event передбачає, що функція `listen` вже викликана на сокеті `target`

`target`

Рядок, ресурс сокету або потік, пов'язаний із сокетом. Якщо параметр `target` - Рядок, то рядок буде розбиратися як мережевий адресу. Вона буде інтерпретована як шлях сокету домену UNIX, якщо міститиме префікс `«unix:»`, например`«unix:/tmp/my.sock»`

### список змін

| Версия | Опис |
| --- | --- |
| PECL event 1.5.0 | Додано підтримку сокетів домену UNIX. |

### Приклади

**Пример #1 Пример использования метода**EventListener::\_\_construct()\*\*\*\*

```php
<?php

/*
 * Простой сервер на основе слушателя соединений модуля libevent.
 *
 * Применение:
 * 1) В одном окне терминала запустите команду:
 *
 * $ php listener.php 9881
 *
 * 2) В другом окне терминала откройте соединение, например:
 *
 * $ nc 127.0.0.1 9881
 *
 * 3) Начните печатать. Сервер должен повторить ввод.
 */

class MyListenerConnection {
    private $bev, $base;

    public function __destruct() {
        $this->bev->free();
    }

    public function __construct($base, $fd) {
        $this->base = $base;

        $this->bev = new EventBufferEvent($base, $fd, EventBufferEvent::OPT_CLOSE_ON_FREE);

        $this->bev->setCallbacks(array($this, "echoReadCallback"), NULL,
            array($this, "echoEventCallback"), NULL);

        if (!$this->bev->enable(Event::READ)) {
            echo "Не удалось включить READ\n";
            return;
        }
    }

    public function echoReadCallback($bev, $ctx) {
        // Скопируйте все данные из входного буфера в выходной буфер

        // Вариант #1
        $bev->output->addBuffer($bev->input);

        /* Вариант #2 */
        /*
        $input    = $bev->getInput();
        $output = $bev->getOutput();
        $output->addBuffer($input);
        */
    }

    public function echoEventCallback($bev, $events, $ctx) {
        if ($events & EventBufferEvent::ERROR) {
            echo "Ошибка bufferevent\n";
        }

        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
            //$bev->free();
            $this->__destruct();
        }
    }
}

class MyListener {
    public $base,
        $listener,
        $socket;
    private $conn = array();

    public function __destruct() {
        foreach ($this->conn as &$c) $c = NULL;
    }

    public function __construct($port) {
        $this->base = new EventBase();
        if (!$this->base) {
            echo "Не удалось открыть событийную базу";
            exit(1);
        }

        // Вариант #1
        /*
        $this->socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
        if (!socket_bind($this->socket, '0.0.0.0', $port)) {
            echo "Невозможно связать сокет\n";
            exit(1);
        }
        $this->listener = new EventListener($this->base,
            array($this, "acceptConnCallback"), $this->base,
            EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE,
            -1, $this->socket);
         */

        // Вариант #2
         $this->listener = new EventListener($this->base,
             array($this, "acceptConnCallback"), $this->base,
             EventListener::OPT_CLOSE_ON_FREE | EventListener::OPT_REUSEABLE, -1,
             "0.0.0.0:$port");

        if (!$this->listener) {
            echo "Не удалось создать слушателя";
            exit(1);
        }

        $this->listener->setErrorCallback(array($this, "accept_error_cb"));
    }

    public function dispatch() {
        $this->base->dispatch();
    }

    // Этот callback вызывается, когда есть данные для чтения на $bev
    public function acceptConnCallback($listener, $fd, $address, $ctx) {
        // Мы получили новое соединение! Создайте для этого все необходимое. */
        $base = $this->base;
        $this->conn[] = new MyListenerConnection($base, $fd);
    }

    public function accept_error_cb($listener, $ctx) {
        $base = $this->base;

        fprintf(STDERR, "Получил ошибку %d (%s) на слушателе."
            ."Выключение.\n",
            EventUtil::getLastSocketErrno(),
            EventUtil::getLastSocketError());

        $base->exit(NULL);
    }
}

$port = 9808;

if ($argc > 1) {
    $port = (int) $argv[1];
}
if ($port <= 0 || $port > 65535) {
    exit("Invalid port");
}

$l = new MyListener($port);
$l->dispatch();

?>
```
