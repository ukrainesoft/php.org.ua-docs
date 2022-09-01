---
navigation:
  - eventbuffer.add.html: '« EventBuffer::add'
  - eventbuffer.appendfrom.html: 'EventBuffer::appendFrom »'
  - index.html: PHP Manual
  - class.eventbuffer.html: EventBuffer
title: 'EventBuffer::addBuffer'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::add()](eventbuffer.add.md) - Додає дані до кінця буфера подій
