---
navigation:
  - gearmantask.taskdenominator.md: '« GearmanTask::taskDenominator'
  - gearmantask.unique.md: 'GearmanTask::unique »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::taskNumerator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::taskNumerator

(PECL gearman >= 0.5.0)

GearmanTask::taskNumerator — Отримання чисельника відсотка виконаної роботи

### Опис

```methodsynopsis
public GearmanTask::taskNumerator(): false|int
```

Повертає чисельник дробу, який використовується для обчислення відсотка виконаної роботи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число от 0 до 100 или\*\*`false`\*\*якщо значення визначити не вдалося.

### Дивіться також

-   [GearmanTask::taskDenominator()](gearmantask.taskdenominator.md) \- отримати знаменник відсотка виконаної роботи
