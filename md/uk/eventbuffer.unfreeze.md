---
navigation:
  - eventbuffer.substr.md: '« EventBuffer::substr'
  - eventbuffer.unlock.md: 'EventBuffer::unlock »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::unfreeze'
---
# EventBuffer::unfreeze

(PECL event >= 1.2.6-beta)

EventBuffer::unfreeze — Повторно включає дзвінки, які змінюють буфер подій

### Опис

```methodsynopsis
public
   EventBuffer::unfreeze(
    bool
     $at_front
   ): bool
```

Повторно включає дзвінки, які змінюють буфер подій.

### Список параметрів

`at_front`

Визначає увімкнути події на початку або в кінці буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::freeze()](eventbuffer.freeze.md) - Запобігає викликам, які змінюють буфер подій у разі успішного виконання
