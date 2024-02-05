---
navigation:
  - gearmantask.isrunning.md: '« GearmanTask::isRunning'
  - gearmantask.recvdata.md: 'GearmanTask::recvData »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::jobHandle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::jobHandle

# gearman\_job\_handle

(PECL gearman >= 0.5.0)

GearmanTask::jobHandle -- gearman\_job\_handle — Отримати дескриптор завдання

### Опис

```methodsynopsis
public GearmanTask::jobHandle(): false|string
```

Повертає дескриптор завдання для цього завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Описувач об'єкта роботи або \*\*`false`\*\*якщо завдання ще не створено.

### Дивіться також

-   [GearmanClient::doJobHandle()](gearmanclient.dojobhandle.md) \- Отримати дескриптор завдання, що виконується
