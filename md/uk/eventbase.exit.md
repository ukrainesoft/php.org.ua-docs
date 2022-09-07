---
navigation:
  - eventbase.dispatch.md: '« EventBase::dispatch'
  - eventbase.free.md: 'EventBase::free »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::exit'
---
# EventBase::exit

(PECL event >= 1.2.6-beta)

EventBase::exit — Припиняє надсилання подій

### Опис

```methodsynopsis
public
   EventBase::exit(
    float
     $timeout
    = ?): bool
```

Повідомляє, що база подій повинна припинити надсилання подій через вказану кількість секунд.

### Список параметрів

`timeout`

Необов'язковий параметр. Кількість секунд, після якого база подій повинна припинити надсилання подій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::stop()](eventbase.stop.md) - Повідомляє eventbase припинити відправку подій
