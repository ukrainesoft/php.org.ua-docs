---
navigation:
  - eventbase.reinit.md: '« EventBase::reInit'
  - class.eventbuffer.md: EventBuffer »
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::stop'
---
# EventBase::stop

(PECL event >= 1.2.6-beta)

EventBase::stop — Повідомляє eventbase припинити відправку подій

### Опис

```methodsynopsis
public
   EventBase::stop(): bool
```

Повідомляє eventbase припинити відправку подій

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::exit()](eventbase.exit.md) - Припиняє відправлення подій
-   [EventBase::gotStop()](eventbase.gotstop.md) - Перевіряє, чи був цикл обробки подій завершений
