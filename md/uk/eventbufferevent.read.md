---
navigation:
  - eventbufferevent.getoutput.md: '« EventBufferEvent::getOutput'
  - eventbufferevent.readbuffer.md: 'EventBufferEvent::readBuffer »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::read

(PECL event >= 1.2.6-beta)

EventBufferEvent::read — Читає дані буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::read(
    int
     $size
   ): string
```

Видаляє до `size` байтів із вхідного буфера. Повертає рядок даних, прочитаний із вхідного буфера.

### Список параметрів

`size`

Максимальна кількість байтів для читання

### Значення, що повертаються

Повертає рядок даних, прочитаний із вхідного буфера.

### Дивіться також

-   [EventBufferEvent::readBuffer()](eventbufferevent.readbuffer.md) \- Зливає весь вміст буфера введення та поміщає його у буфер
