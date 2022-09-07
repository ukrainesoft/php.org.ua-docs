---
navigation:
  - eventbufferevent.sslsocket.md: '« EventBufferEvent::sslSocket'
  - eventbufferevent.writebuffer.md: 'EventBufferEvent::writeBuffer »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
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

-   [EventBufferEvent::writeBuffer()](eventbufferevent.writebuffer.md) - Додає вміст буфера в буфер виведення буферної події
