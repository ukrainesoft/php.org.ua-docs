---
navigation:
  - eventbuffer.unfreeze.md: '« EventBuffer::unfreeze'
  - eventbuffer.write.md: 'EventBuffer::write »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::unlock'
---
# EventBuffer::unlock

(PECL event >= 1.2.6-beta)

EventBuffer::unlock — Знімає блокування, встановлене EventBuffer::lock

### Опис

```methodsynopsis
public
   EventBuffer::unlock(): bool
```

Знімає блокування, встановлене [EventBuffer::lock()](eventbuffer.lock.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::lock()](eventbuffer.lock.md) - Отримує блокування буфера
