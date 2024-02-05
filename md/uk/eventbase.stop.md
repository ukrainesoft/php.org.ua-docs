---
navigation:
  - eventbase.reinit.md: '« EventBase::reInit'
  - class.eventbuffer.md: EventBuffer »
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::stop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBase::stop

(PECL event >= 1.2.6-beta)

EventBase::stop — Повідомляє event\_base припинити відправку подій

### Опис

```methodsynopsis
public
   EventBase::stop(): bool
```

Повідомляє event\_base припинити відправку подій

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBase::exit()](eventbase.exit.md) \- Припиняє відправлення подій
-   [EventBase::gotStop()](eventbase.gotstop.md) \- Перевіряє, чи був цикл обробки подій завершений
