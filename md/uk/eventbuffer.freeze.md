---
navigation:
  - eventbuffer.expand.md: '« EventBuffer::expand'
  - eventbuffer.lock.md: 'EventBuffer::lock »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::freeze'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBuffer::freeze

(PECL event >= 1.2.6-beta)

EventBuffer::freeze — Запобігає викликам, які змінюють буфер подій у разі успішного виконання

### Опис

```methodsynopsis
public
   EventBuffer::freeze(
    bool
     $at_front
   ): bool
```

Запобігає викликам, які змінюють буфер подій у разі успішного виконання

### Список параметрів

`at_front`

Чи вимкнути зміни на початку або в кінці буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBuffer::unfreeze()](eventbuffer.unfreeze.md) \- Повторно включає дзвінки, які змінюють буфер подій
