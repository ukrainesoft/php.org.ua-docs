---
navigation:
  - eventbufferevent.connect.md: '« EventBufferEvent::connect'
  - eventbufferevent.construct.md: 'EventBufferEvent::construct »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::connectHost'
---
# EventBufferEvent::connectHost

(PECL event >= 1.2.6-beta)

EventBufferEvent::connectHost — Підключається на ім'я хоста з можливістю асинхронного дозволу DNS

### Опис

```methodsynopsis
public
   EventBufferEvent::connectHost(    
    EventDnsBase
     $dns_base
   ,    
    string
     $hostname
   ,    
    int
     $port
   ,    
    int
     $family
     = EventUtil::AF_UNSPEC
   ): bool
```

Дозволяє ім'я хоста DNS-імені, шукаючи адреси типу `family` (Константи `EventUtil::AF_*`). Якщо дозвіл імені не вдалося зробити, викликає callback-функцію події з подією помилки. У разі успішного виконання робить спробу підключення так само, як [EventBufferEvent::connect()](eventbufferevent.connect.md)

Параметр `dns_base` не є обов'язковим. Він може мати значення **`null`** або посилатися на об'єкт, створений за допомогою [EventDnsBase::construct()](eventdnsbase.construct.md). Для асинхронного дозволу імені хоста необхідно передати дійсний базовий ресурс події DNS. В іншому випадку дозвіл імені хоста буде заблоковано.

> **Зауваження**
> 
> [EventDnsBase](class.eventdnsbase.md) доступний, тільки якщо `Event` налаштований з **\-with-event-extra** (бібліотека `event_extra` *підтримка функцій протоколу libevent, включаючи HTTP, DNS та RPC*

> **Зауваження**
> 
> **EventBufferEvent::connectHost()** вимагає `libevent-2.0.3-alpha` або вище.

### Список параметрів

`dns_base`

Об'єкт [EventDnsBase](class.eventdnsbase.md) у випадку, якщо DNS потрібно дозволити асинхронно . **`null`** в іншому випадку.

`hostname`

Ім'я хоста для підключення. Формати, що розпізнаються:

[www.example.com](http://www.example.com) (hostname) 1.2.3.4 (ipv4address) ::1 (ipv6address) ipv6address

`port`

Номер порту.

`family`

Сімейство адрес . **`EventUtil::AF_UNSPEC`** **`EventUtil::AF_INET`** або **`EventUtil::AF_INET6`**. Зверніться до списку [констант EventUtil](class.eventutil.html#eventutil.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 **Приклад використання EventBufferEvent::connectHost()****

```php
<?php
/* Callback-функция чтения */
function readcb($bev, $base) {
    //$input = $bev->input; //$bev->getInput();

    //$pos = $input->search("TTP");
    $pos = $bev->input->search("TTP");

    while (($n = $bev->input->remove($buf, 1024)) > 0) {
        echo $buf;
    }
}

/* Callback-функция события */
function eventcb($bev, $events, $base) {
    if ($events & EventBufferEvent::CONNECTED) {
        echo "Подключено.\n";
    } elseif ($events & (EventBufferEvent::ERROR | EventBufferEvent::EOF)) {
        if ($events & EventBufferEvent::ERROR) {
            echo "Ошибка DNS: ", $bev->getDnsErrorString(), PHP_EOL;
        }

        echo "Закрытие\n";
        $base->exit();
        exit("Выполнено\n");
    }
}

$base = new EventBase();

$dns_base = new EventDnsBase($base, TRUE); // Использование асинхронного разрешения DNS
if (!$dns_base) {
    exit("Не удалось запустить базу DNS\n");
}

$bev = new EventBufferEvent($base, /* использование внутреннего сокета */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,
    "readcb", /* writecb */ NULL, "eventcb", $base
);
if (!$bev) {
    exit("Не удалось создать сокет bufferevent\n");
}

//$bev->setCallbacks("readcb", /* writecb */ NULL, "eventcb", $base);
$bev->enable(Event::READ | Event::WRITE);

$output = $bev->output; //$bev->getOutput();
if (!$output->add(
    "GET {$argv[2]} HTTP/1.0\r\n".
    "Host: {$argv[1]}\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Не удалось добавить запрос в выходной буфер\n");
}

if (!$bev->connectHost($dns_base, $argv[1], 80, EventUtil::AF_UNSPEC)) {
    exit("Не удалось подключиться к хосту {$argv[1]}\n");
}

$base->dispatch();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Connected.
HTTP/1.0 301 Moved Permanently
Location: http://www.google.co.uk/
Content-Type: text/html; charset=UTF-8
Date: Sat, 09 Mar 2013 12:21:19 GMT
Expires: Mon, 08 Apr 2013 12:21:19 GMT
Cache-Control: public, max-age=2592000
Server: gws
Content-Length: 221
X-XSS-Protection: 1; mode=block
X-Frame-Options: SAMEORIGIN

<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.co.uk/">here</A>.
</BODY></HTML>
Closing
Done
```

### Дивіться також

-   [EventBufferEvent::connect()](eventbufferevent.connect.md) - Підключає файловий дескриптор події буфера до вказаної адреси або сокету UNIX
