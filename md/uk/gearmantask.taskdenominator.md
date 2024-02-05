---
navigation:
  - gearmantask.sendworkload.md: '« GearmanTask::sendWorkload'
  - gearmantask.tasknumerator.md: 'GearmanTask::taskNumerator »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::taskDenominator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::taskDenominator

(PECL gearman >= 0.5.0)

GearmanTask::taskDenominator — Отримати знаменник відсотка виконаної роботи

### Опис

```methodsynopsis
public GearmanTask::taskDenominator(): false|int
```

Отримує знаменник дробу, що використовується визначення відсотка виконаної роботи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число от 0 до 100 или\*\*`false`\*\*якщо визначити значення не вдалося.

### Дивіться також

-   [GearmanTask::taskNumerator()](gearmantask.tasknumerator.md) \- отримання чисельника відсотка виконаної роботи
