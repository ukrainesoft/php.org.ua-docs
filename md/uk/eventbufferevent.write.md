---
navigation:
  - eventbufferevent.sslsocket.html: '« EventBufferEvent::sslSocket'
  - eventbufferevent.writebuffer.html: 'EventBufferEvent::writeBuffer »'
  - index.html: PHP Manual
  - class.eventbufferevent.html: EventBufferEvent
title: 'EventBufferEvent::write'
---
# EventBufferEvent::write

(PECL event >= 1.2.6-beta)

EventBufferEvent::write — Додає дані до буфера виводу буферної події

### Опис

```methodsynopsis
public
   EventBufferEvent::write(
    string
     $data
   ): bool
```

Додає `data` у буфер виведення буферної події

### Список параметрів

`data`

Дані для додавання до базового буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBufferEvent::writeBuffer()](eventbufferevent.writebuffer.html) - Додає вміст буфера в буфер виведення буферної події
