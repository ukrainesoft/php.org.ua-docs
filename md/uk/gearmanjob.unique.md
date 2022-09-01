---
navigation:
  - gearmanjob.status.md: '« GearmanJob::status'
  - gearmanjob.warning.md: 'GearmanJob::warning »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::unique'
---
# GearmanJob::unique

(PECL gearman >= 0.5.0)

GearmanJob::unique — Отримання унікального ідентифікатора

### Опис

```methodsynopsis
public GearmanJob::unique(): string
```

Повертає унікальний ідентифікатор завдання, наданий клієнтом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) - Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanTask::uuid()](gearmantask.uuid.md) - отримання унікального ідентифікатора завдання (застарілий метод)
