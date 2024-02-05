---
navigation:
  - eventbuffer.add.md: '« EventBuffer::add'
  - eventbuffer.appendfrom.md: 'EventBuffer::appendFrom »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::addBuffer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::addBuffer

(PECL event >= 1.2.6-beta)

EventBuffer::addBuffer — Переміщує всі дані з буфера екземпляру EventBuffer

### Опис

```methodsynopsis
public
   EventBuffer::addBuffer(
    EventBuffer
     $buf
   ): bool
```

Переміщує всі дані з буфера, вказаного у параметрі `buf`, в кінець поточного [EventBuffer](class.eventbuffer.md). Це руйнівний додаток. Дані з одного буфера переміщуються до іншого буфера. Однак, непотрібних копій пам'яті не відбувається.

### Список параметрів

`buf`

Вихідний об'єкт EventBuffer.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::add()](eventbuffer.add.md) \- Додає дані до кінця буфера подій
