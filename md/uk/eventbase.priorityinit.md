---
navigation:
  - eventbase.loop.html: '« EventBase::loop'
  - eventbase.reinit.html: 'EventBase::reInit »'
  - index.html: PHP Manual
  - class.eventbase.html: EventBase
title: 'EventBase::priorityInit'
---
# EventBase::priorityInit

(PECL event >= 1.2.6-beta)

EventBase::priorityInit — Встановлює кількість пріоритетів на базі подій

### Опис

```methodsynopsis
public
   EventBase::priorityInit(
    int
     $n_priorities
   ): bool
```

Встановлює кількість пріоритетів на основі подій

### Список параметрів

`n_priorities`

Кількість пріоритетів з урахуванням подій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Event::setPriority()](event.setpriority.html) - Задати пріоритет події
