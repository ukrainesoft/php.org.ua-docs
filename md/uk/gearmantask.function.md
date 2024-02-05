---
navigation:
  - gearmantask.datasize.md: '« GearmanTask::dataSize'
  - gearmantask.functionname.md: 'GearmanTask::functionName »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::function'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::function

(PECL gearman <= 0.5.0)

GearmanTask::function — Отримати ім'я пов'язаної функції (застарілий метод)

### Опис

```methodsynopsis
public GearmanTask::function(): string
```

Повертає ім'я функції, з якою пов'язане це завдання. Цю функцію викликає обробник у процесі роботи з даними.

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanTask::functionName()](gearmantask.functionname.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я функції.
