---
navigation:
  - eventbuffer.unfreeze.md: '« EventBuffer::unfreeze'
  - eventbuffer.write.md: 'EventBuffer::write »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::unlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::unlock

(PECL event >= 1.2.6-beta)

EventBuffer::unlock — Знімає блокування, встановлене EventBuffer::lock

### Опис

```methodsynopsis
public
   EventBuffer::unlock(): bool
```

Снимает блокировку, установленную[EventBuffer::lock()](eventbuffer.lock.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::lock()](eventbuffer.lock.md) \- Отримує блокування буфера
