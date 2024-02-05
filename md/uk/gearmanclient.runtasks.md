---
navigation:
  - gearmanclient.returncode.md: '« GearmanClient::returnCode'
  - gearmanclient.setclientcallback.md: 'GearmanClient::setClientCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::runTasks'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::runTasks

(PECL gearman >= 0.5.0)

GearmanClient::runTasks — Запустити список завдань у паралельному режимі

### Опис

```methodsynopsis
public GearmanClient::runTasks(): bool
```

Для набору завдань, раніше доданих за допомогою [GearmanClient::addTask()](gearmanclient.addtask.md) [GearmanClient::addTaskHigh()](gearmanclient.addtaskhigh.md) [GearmanClient::addTaskLow()](gearmanclient.addtasklow.md) [GearmanClient::addTaskBackground()](gearmanclient.addtaskbackground.md) [GearmanClient::addTaskHighBackground()](gearmanclient.addtaskhighbackground.md) або [GearmanClient::addTaskLowBackground()](gearmanclient.addtasklowbackground.md), цей виклик починається в паралельному режимі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanClient::addTask()](gearmanclient.addtask.md) \- Додати завдання, яке буде виконано у паралельному режимі
