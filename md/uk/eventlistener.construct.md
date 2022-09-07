---
navigation:
  - class.eventlistener.md: « EventListener
  - eventlistener.disable.md: 'EventListener::disable »'
  - index.md: PHP Manual
  - class.eventlistener.md: EventListener
title: 'EventListener::construct'
---
# EventListener::construct

(PECL event >= 1.2.6-beta)

EventListener::construct — Створити новий слухач з'єднання, пов'язаний із базою подій

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

Створює новий слухач з'єднання, пов'язаний із базою подій.

### Список параметрів

`base`

Подієва база.

`cb`

Callback-функція ([callable](language.types.callable.md)), яка буде викликана при отриманні з'єднання.

`data`

Дані користувача, які будуть передаватися в `cb`

`flags`

Бітова маска з констант `EventListener::OPT_*`. Дивіться [константи EventListener](class.eventlistener.md#eventlistener.constants)

`backlog`

Встановлює максимальну кількість очікуваних з'єднань, яким, мережевим стеком, можна чекати в стані ще не прийнято. Докладніше дивіться у документації щодо системної функції `listen`. Якщо значення `backlog` негативно, Libevent спробує самостійно вибрати найкраще значення для `backlog`. Якщо дорівнює нулю, Event вважатиме, що `listen` вже викликана на сокеті( `target`

`target`

Може бути рядком, ресурсом сокету або потоком, пов'язаним із сокетом. Якщо `target` є рядком, вона буде розбиратися як мережевий адресу. Вона інтерпретуватиметься як шлях сокету домену UNIX, якщо матиме префікс `'unix:'` , наприклад, `'unix:/tmp/my.sock'`

### Значення, що повертаються

Повертає об'єкт [EventListener](class.eventlistener.md), що представляє слухач події з'єднання.

### список змін

| Версия | Описание |
| --- | --- |
| PECL event 1.5.0 | Додано підтримку сокетів домену UNIX. |

### Приклади

**Приклад #1 Приклад використання **EventListener::construct()****

```php
<?php
/*
 * Простой сервер на основе прослушивателя соединений libevent.
 *
 * Использование:
 * 1) В одном окне терминала запустите:
 *
 * $ php listener.php 9881
 *
 * 2) В другом окне терминала откройте соединение, например:
 *
 * $ nc 127.0.0.1 9881
 *
 * 3) начните печатать. Сервер должен повторить ввод.
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
