---
navigation:
  - eventbase.gettimeofdaycached.md: '« EventBase::getTimeOfDayCached'
  - eventbase.gotstop.md: 'EventBase::gotStop »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::gotExit'
---
# EventBase::gotExit

(PECL event >= 1.2.6-beta)

EventBase::gotExit — Перевіряє, чи завершився цикл обробки подій.

### Опис

```methodsynopsis
public
   EventBase::gotExit(): bool
```

Перевіряє, чи був цикл обробки подій завершено за допомогою [EventBase::exit()](eventbase.exit.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цикл обробки подій завершено за допомогою [EventBase::exit()](eventbase.exit.md) . В інших випадках – **`false`**

### Дивіться також

-   [EventBase::exit()](eventbase.exit.md) - Припиняє відправлення подій
-   [EventBase::stop()](eventbase.stop.md) - Повідомляє eventbase припинити відправку подій
-   [EventBase::gotStop()](eventbase.gotstop.md) - Перевіряє, чи був цикл обробки подій завершений
