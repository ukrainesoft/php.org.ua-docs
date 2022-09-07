---
navigation:
  - gearmantask.sendworkload.md: '« GearmanTask::sendWorkload'
  - gearmantask.tasknumerator.md: 'GearmanTask::taskNumerator »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::taskDenominator'
---
# GearmanTask::taskDenominator

(PECL gearman >= 0.5.0)

GearmanTask::taskDenominator — Отримати знаменник відсотка виконаної роботи

### Опис

```methodsynopsis
public GearmanTask::taskDenominator(): int
```

Отримує знаменник дробу, що використовується визначення відсотка виконаної роботи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число від 0 до 100 або \*\*`false`\*\*якщо визначити значення не вдалося.

### Дивіться також

-   [GearmanTask::taskNumerator()](gearmantask.tasknumerator.md) - отримання чисельника відсотка виконаної роботи
