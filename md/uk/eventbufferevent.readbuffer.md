---
navigation:
  - eventbufferevent.read.md: '« EventBufferEvent::read'
  - eventbufferevent.setcallbacks.md: 'EventBufferEvent::setCallbacks »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::readBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::readBuffer

(PECL event >= 1.2.6-beta)

EventBufferEvent::readBuffer — Зливає весь вміст буфера введення та поміщає його в буфер

### Опис

```methodsynopsis
public
   EventBufferEvent::readBuffer(
    EventBuffer
     $buf
   ): bool
```

Зливає весь вміст буфера введення і поміщає його в `buf`

### Список параметрів

`buf`

Цільовий буфер

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBufferEvent::read()](eventbufferevent.read.md) \- Читає дані буфера
