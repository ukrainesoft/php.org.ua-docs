---
navigation:
  - eventbuffer.copyout.md: '« EventBuffer::copyout'
  - eventbuffer.enablelocking.md: 'EventBuffer::enableLocking »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::drain'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::drain

(PECL event >= 1.2.6-beta)

EventBuffer::drain — Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи

### Опис

```methodsynopsis
public
   EventBuffer::drain(
    int
     $len
   ): bool
```

Поводиться, як [EventBuffer::read()](eventbuffer.read.md), За винятком того, що він не копіює дані: просто видаляє їх з початку буфера.

### Список параметрів

`len`

Кількість байтів видалення з буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.md) \- Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) \- Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
