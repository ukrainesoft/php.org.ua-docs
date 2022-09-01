---
navigation:
  - eventbufferevent.close.html: '« EventBufferEvent::close'
  - eventbufferevent.connecthost.html: 'EventBufferEvent::connectHost »'
  - index.html: PHP Manual
  - class.eventbufferevent.html: EventBufferEvent
title: 'EventBufferEvent::connect'
---
# EventBufferEvent::connect

(PECL event >= 1.2.6-beta)

EventBufferEvent::connect — Підключає файловий дескриптор події буфера до вказаної адреси або сокету UNIX

### Опис

```methodsynopsis
public
   EventBufferEvent::connect(
    string
     $addr
   ): bool
```

Підключає файловий дескриптор події буфера до вказаної адреси (опційно з портом) або UNIX-сокету.

Якщо сокет не призначений для події буфера, функція виділяє новий сокет і робить його внутрішнім неблокуючим.

Щоб дозволити DNS-імена (асинхронно), використовуйте метод [EventBufferEvent::connectHost()](eventbufferevent.connecthost.html)

### Список параметрів

`addr`

Повинна містити IP-адресу з необов'язковим номером порту або шлях до сокету домену UNIX. Допустимі формати:

IPv6Address:portIPv6AddressIPv6Address IPv4Address:port IPv4Address unix:path

Майте на увазі, що префікс `'unix:'` нині не чутливий до регістру.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **EventBufferEvent::connect()****

```php
<?php
/*
 * 1. Подключение к 127.0.0.1 и порту 80
 * by means of EventBufferEvent::connect().
 *
 * 2. Запрос /index.cphp с помощью HTTP/1.0
 * используя выходной буфер.
 *
 * 3. Асинхронно прочитайте ответ и распечатайте его стандартным выводом.
 */

/* Чтение callback-функции */
function readcb($bev, $base) {
    $input = $bev->getInput();

    while (($n = $input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}

/* Событие callback-функции */
function eventcb($bev, $events, $base) {
    if ($events & EventBufferEvent::CONNECTED) {
        echo "Подключено.\n";
    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {
        if ($events & EventBufferEvent::ERROR) {
            echo "DNS ошибка: ", $bev->getDnsErrorString(), PHP_EOL;
        }

        echo "Закрытие\n";
        $base->exit();
        exit("Завершено\n");
    }
}

$base = new EventBase();

echo "шаг 1\n";
$bev = new EventBufferEvent($base, /* используйте внутренний сокет */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS);
if (!$bev) {
    exit("Не удалось создать сокет bufferevent\n");
}

echo "шаг 2\n";
$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);
$bev->enable(Event::READ | Event::WRITE);

echo "шаг 3\n";
/* Послать запрос */
$output = $bev->getOutput();
if (!$output->add(
    "GET /index.cphp HTTP/1.0\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Не удалось добавить запрос в выходной буфер\n");
}

/* Подключение к хосту синхронно.
 * Мы знаем IP, и нам не нужно разрешать DNS. */
if (!$bev->connect("127.0.0.1:80")) {
    exit("Не удаётся подключиться к хосту\n");
}

/* Отправка ожидающих событий */
$base->dispatch();
```

Результатом виконання цього прикладу буде щось подібне:

```
step 1
step 2
step 3
Connected.
HTTP/1.1 200 OK
Server: nginx/1.2.6
Date: Sat, 09 Mar 2013 10:06:58 GMT
Content-Type: text/html; charset=utf-8
Connection: close
X-Powered-By: PHP/5.4.11--pl2-gentoo

sdfsdfsf
Closing
Done
```

**Приклад #2 Підключіться до сокету домену UNIX, який імовірно обслуговується сервером, прочитайте відповідь сервера та виведіть його на консоль**

```php
<?php
class MyUnixSocketClient {
    private $base, $bev;

    function __construct($base, $sock_path) {
        $this->base = $base;
        $this->bev = new EventBufferEvent($base, NULL, EventBufferEvent::OPT_CLOSE_ON_FREE,
            array ($this, "read_cb"), NULL, array ($this, "event_cb"));

        if (!$this->bev->connect("unix:$sock_path")) {
            trigger_error("Failed to connect to socket `$sock_path'", E_USER_ERROR);
        }

        $this->bev->enable(Event::READ);
    }

    function __destruct() {
        if ($this->bev) {
            $this->bev->free();
            $this->bev = NULL;
        }
    }

    function dispatch() {
        $this->base->dispatch();
    }

    function read_cb($bev, $unused) {
        $in = $bev->input;

        printf("Получено %ld байтов\n", $in->length);
        printf("----- данные ----\n");
        printf("%ld:\t%s\n", (int) $in->length, $in->pullup(-1));

        $this->bev->free();
        $this->bev = NULL;
        $this->base->exit(NULL);
    }

    function event_cb($bev, $events, $unused) {
        if ($events & EventBufferEvent::ERROR) {
            echo "Ошибка bufferevent\n";
        }

        if ($events & (EventBufferEvent::EOF | EventBufferEvent::ERROR)) {
            $bev->free();
            $bev = NULL;
        } elseif ($events & EventBufferEvent::CONNECTED) {
            $bev->output->add("test\n");
        }
    }
}

if ($argc <= 1) {
    exit("Путь к сокету не указан\n");
}
$sock_path = $argv[1];

$base = new EventBase();
$cl = new MyUnixSocketClient($base, $sock_path);
$cl->dispatch();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Получено 5 байтов
----- данные ----
5:  test
```

### Дивіться також

-   [EventBufferEvent::connectHost()](eventbufferevent.connecthost.html) - Підключається на ім'я хоста з можливістю асинхронного дозволу DNS
