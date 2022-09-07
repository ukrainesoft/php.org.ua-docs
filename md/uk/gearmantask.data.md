---
navigation:
  - gearmantask.create.md: '« GearmanTask::create'
  - gearmantask.datasize.md: 'GearmanTask::dataSize »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::data'
---
# GearmanTask::data

(PECL gearman >= 0.5.0)

GearmanTask::data — Отримати дані, повернені для завдання

### Опис

```methodsynopsis
public GearmanTask::data(): string
```

Отримує дані, що повертаються обробником після завершення роботи завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Серіалізовані дані або \*\*`false`\*\*якщо обробник не надав даних.

### Дивіться також

-   [GearmanTask::dataSize()](gearmantask.datasize.md) - Отримати розмір даних, що повертаються
