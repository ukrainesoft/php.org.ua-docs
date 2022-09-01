---
navigation:
  - eventbase.gotexit.md: '« EventBase::gotExit'
  - eventbase.loop.md: 'EventBase::loop »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::gotStop'
---
# EventBase::gotStop

(PECL event >= 1.2.6-beta)

EventBase::gotStop — Перевіряє, чи завершився цикл обробки подій.

### Опис

```methodsynopsis
public
   EventBase::gotStop(): bool
```

Перевіряє, чи був цикл обробки подій завершено за допомогою [EventBase::stop()](eventbase.stop.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо цикл обробки подій було завершено за допомогою [EventBase::stop()](eventbase.stop.md) . В іншому випадку - **`false`**

### Дивіться також

-   [EventBase::exit()](eventbase.exit.md) - Припиняє відправлення подій
-   [EventBase::stop()](eventbase.stop.md) - Повідомляє eventbase припинити відправку подій
-   [EventBase::gotExit()](eventbase.gotexit.md) - Перевіряє, чи був цикл обробки подій завершений
