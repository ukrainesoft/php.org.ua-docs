---
navigation:
  - gearmanjob.fail.md: '« GearmanJob::fail'
  - gearmanjob.handle.md: 'GearmanJob::handle »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::functionName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::functionName

(PECL gearman >= 0.5.0)

GearmanJob::functionName — Отримання імені функції

### Опис

```methodsynopsis
public GearmanJob::functionName(): false|string
```

Повертає ім'я функції, яка обробляє дані, тобто функції, яка буде викликана для виконання завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Имя функции или\*\*`false`\*\*якщо завдання ще не ініціалізоване.

### Дивіться також

-   [GearmanTask::function()](gearmantask.function.md) \- Отримати ім'я пов'язаної функції (застарілий метод)
