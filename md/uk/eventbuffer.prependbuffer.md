---
navigation:
  - eventbuffer.prepend.md: '« EventBuffer::prepend'
  - eventbuffer.pullup.md: 'EventBuffer::pullup »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::prependBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::prependBuffer

(PECL event >= 1.2.6-beta)

EventBuffer::prependBuffer — Переміщує всі дані з вихідного буфера на початок поточного буфера

### Опис

```methodsynopsis
public
   EventBuffer::prependBuffer(
    EventBuffer
     $buf
   ): bool
```

Поводиться як [EventBuffer::addBuffer()](eventbuffer.addbuffer.md) , За винятком того, що він переміщає дані на початок буфера.

### Список параметрів

`buf`

Початковий буфер.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::add()](eventbuffer.add.md) \- Додає дані до кінця буфера подій
-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.md) \- Переміщує всі дані з буфера екземпляру EventBuffer
-   [EventBuffer::prepend()](eventbuffer.prepend.md) \- Записує дані на початок буфера
