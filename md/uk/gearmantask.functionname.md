---
navigation:
  - gearmantask.function.md: '« GearmanTask::function'
  - gearmantask.isknown.md: 'GearmanTask::isKnown »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::functionName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::functionName

(PECL gearman >= 0.6.0)

GearmanTask::functionName — Отримати назву функції

### Опис

```methodsynopsis
public GearmanTask::functionName(): false|string
```

Повертає ім'я функції, з якою пов'язане завдання. Цю функцію викликає обробник у процесі роботи з даними.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Имя функции или\*\*`false`\*\*якщо завдання ще не створено.
