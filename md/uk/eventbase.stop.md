---
navigation:
  - eventbase.reinit.html: '« EventBase::reInit'
  - class.eventbuffer.html: EventBuffer »
  - index.html: PHP Manual
  - class.eventbase.html: EventBase
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

-   [EventBase::exit()](eventbase.exit.html) - Припиняє відправлення подій
-   [EventBase::gotStop()](eventbase.gotstop.html) - Перевіряє, чи був цикл обробки подій завершений
