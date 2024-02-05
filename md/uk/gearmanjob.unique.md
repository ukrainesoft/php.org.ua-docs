---
navigation:
  - gearmanjob.status.md: '« GearmanJob::status'
  - gearmanjob.warning.md: 'GearmanJob::warning »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::unique'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::unique

(PECL gearman >= 0.5.0)

GearmanJob::unique — Отримання унікального ідентифікатора

### Опис

```methodsynopsis
public GearmanJob::unique(): false|string
```

Повертає унікальний ідентифікатор завдання, наданий клієнтом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор або \*\*`false`\*\*якщо завдання ще не ініціалізоване.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) \- Виконує одне завдання та повертає результат\[Застарілий метод\]
-   [GearmanTask::uuid()](gearmantask.uuid.md) \- отримання унікального ідентифікатора завдання (застарілий метод)
