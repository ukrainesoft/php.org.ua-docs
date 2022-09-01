---
navigation:
  - gearmantask.tasknumerator.md: '« GearmanTask::taskNumerator'
  - gearmantask.uuid.md: 'GearmanTask::uuid »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::unique'
---
# GearmanTask::unique

(PECL gearman >= 0.6.0)

GearmanTask::unique — Отримання унікального ідентифікатора задачі

### Опис

```methodsynopsis
public GearmanTask::unique(): string
```

Повертає унікальний ідентифікатор цього завдання. Цей ідентифікатор надає [GearmanClient](class.gearmanclient.md), на відміну дескриптора завдання, який встановлює сервер завдань Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор або \*\*`false`\*\*якщо ідентифікатор не присвоєний.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) - Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanClient::addTask()](gearmanclient.addtask.md) - Додати завдання, яке буде виконано у паралельному режимі
