---
navigation:
  - gearmantask.unique.md: '« GearmanTask::unique'
  - class.gearmanworker.md: GearmanWorker »
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::uuid'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::uuid

(PECL gearman <= 0.5.0)

GearmanTask::uuid — Отримання унікального ідентифікатора завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanTask::uuid(): string
```

Повертає унікальний ідентифікатор цього завдання. Цей ідентифікатор надає [GearmanClient](class.gearmanclient.md), на відміну ідентифікатора об'єкта завдання, який встановлює сервер завдань.

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanTask::unique()](gearmantask.unique.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор або \*\*`false`\*\*якщо ідентифікатор не призначений.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) \- Виконує одне завдання та повертає результат\[Застарілий метод\]
-   [GearmanClient::addTask()](gearmanclient.addtask.md) \- Додати завдання, яке буде виконано у паралельному режимі
