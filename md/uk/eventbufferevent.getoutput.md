---
navigation:
  - eventbufferevent.getinput.md: '« EventBufferEvent::getInput'
  - eventbufferevent.read.md: 'EventBufferEvent::read »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::getOutput'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::getOutput

(PECL event >= 1.2.6-beta)

EventBufferEvent::getOutput — Повертає базовий вихідний буфер, пов'язаний із поточною буферною подією

### Опис

```methodsynopsis
public
   EventBufferEvent::getOutput(): EventBuffer
```

Повертає базовий вихідний буфер, пов'язаний із поточною буферною подією. Вихідний буфер є сховищем даних для запису.

Зверніть увагу, що є також `[output](class.eventbufferevent.md#eventbufferevent.props.output)`свойство класса[EventBufferEvent](class.eventbufferevent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр [EventBuffer](class.eventbuffer.md) вихідного буфера, пов'язаного з поточною буферною подією.

### Приклади

**Приклад #1 Приклад використання** EventBufferEvent::getOutput()\*\*\*\*

```php
<?php
$base = new EventBase();

$dns_base = new EventDnsBase($base, TRUE); // Использовать асинхронное разрешение DNS
if (!$dns_base) {
    exit("Не удалось инициализировать базу DNS\n");
}

$bev = new EventBufferEvent($base, /* использовать внутренний сокет */ NULL,
    EventBufferEvent::OPT_CLOSE_ON_FREE | EventBufferEvent::OPT_DEFER_CALLBACKS,
    "readcb", /* writecb */ NULL, "eventcb", $base
);
if (!$bev) {
    exit("Не удалось создать сокет bufferevent\n");
}

$bev->enable(Event::READ | Event::WRITE);

$output = $bev->getOutput();
if (!$output->add(
    "GET {$argv[2]} HTTP/1.0\r\n".
    "Host: {$argv[1]}\r\n".
    "Connection: Close\r\n\r\n"
)) {
    exit("Не удалось добавить запрос в выходной буфер\n");
}

/* ... */
?>
```

### Дивіться також

-   [EventBufferEvent::getInput()](eventbufferevent.getinput.md) \- Повертає базовий вхідний буфер, пов'язаний із поточною буферною подією
