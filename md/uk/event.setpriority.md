---
navigation:
  - event.set.md: '« Event::set'
  - event.settimer.md: 'Event::setTimer »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::setPriority'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::setPriority

(PECL event >= 1.2.6-beta)

Event::setPriority — Задати пріоритет події

### Опис

```methodsynopsis
public
   Event::setPriority(
    int
     $priority
   ): bool
```

Встановлює пріоритет події.

### Список параметрів

`priority`

Пріоритет.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
