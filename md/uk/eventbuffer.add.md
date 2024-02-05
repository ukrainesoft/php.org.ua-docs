---
navigation:
  - class.eventbuffer.md: « EventBuffer
  - eventbuffer.addbuffer.md: 'EventBuffer::addBuffer »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::add'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::add

(PECL event >= 1.2.6-beta)

EventBuffer::add — Додає дані до кінця буфера подій

### Опис

```methodsynopsis
public
   EventBuffer::add(
    string
     $data
   ): bool
```

Додає дані до кінця буфера подій

### Список параметрів

`data`

Рядок, який буде додано в кінець буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.md) \- Переміщує всі дані з буфера екземпляру EventBuffer
