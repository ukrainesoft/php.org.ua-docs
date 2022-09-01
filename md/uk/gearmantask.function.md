---
navigation:
  - gearmantask.datasize.html: '« GearmanTask::dataSize'
  - gearmantask.functionname.html: 'GearmanTask::functionName »'
  - index.html: PHP Manual
  - class.gearmantask.html: GearmanTask
title: 'GearmanTask::function'
---
# GearmanTask::function

(PECL gearman <= 0.5.0)

GearmanTask::function — Отримати ім'я пов'язаної функції (застарілий метод)

### Опис

```methodsynopsis
public GearmanTask::function(): string
```

Повертає ім'я функції, з якою пов'язане це завдання. Цю функцію викликає обробник у процесі роботи з даними.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanTask::functionName()](gearmantask.functionname.html) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ім'я функції.
