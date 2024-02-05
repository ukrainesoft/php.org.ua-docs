---
navigation:
  - eventbuffer.lock.md: '« EventBuffer::lock'
  - eventbuffer.prependbuffer.md: 'EventBuffer::prependBuffer »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::prepend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::prepend

(PECL event >= 1.2.6-beta)

EventBuffer::prepend — Записує дані на початок буфера

### Опис

```methodsynopsis
public
   EventBuffer::prepend(
    string
     $data
   ): bool
```

Записує дані на початок буфера.

### Список параметрів

`data`

Рядок, який буде додано на початок буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::prependBuffer()](eventbuffer.prependbuffer.md) \- Переміщує всі дані з вихідного буфера на початок поточного буфера
-   [EventBuffer::add()](eventbuffer.add.md) \- Додає дані до кінця буфера подій
-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.md) \- Переміщує всі дані з буфера екземпляру EventBuffer
