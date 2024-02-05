---
navigation:
  - eventbufferevent.write.md: '« EventBufferEvent::write'
  - eventbufferevent.about.callbacks.md: Про callback-функції подійного буфера
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::writeBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::writeBuffer

(PECL event >= 1.2.6-beta)

EventBufferEvent::writeBuffer — Додає вміст всього буфера до буфера виводу буферної події

### Опис

```methodsynopsis
public
   EventBufferEvent::writeBuffer(
    EventBuffer
     $buf
   ): bool
```

Додає вміст буфера в буфер виведення буферної події.

### Список параметрів

`buf`

Вихідний об'єкт [EventBuffer](class.eventbuffer.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBufferEvent::write()](eventbufferevent.write.md) \- Додає дані до буфера виводу буферної події
