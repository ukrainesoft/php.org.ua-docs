---
navigation:
  - gearmanjob.functionname.md: '« GearmanJob::functionName'
  - gearmanjob.returncode.md: 'GearmanJob::returnCode »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::handle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::handle

(PECL gearman >= 0.5.0)

GearmanJob::handle — Отримання дескриптора об'єкта завдання

### Опис

```methodsynopsis
public GearmanJob::handle(): false|string
```

Повертає дескриптор завдання, наданий сервером.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дескриптор завдання або \*\*`false`\*\*якщо завдання ще не ініціалізоване.

### Дивіться також

-   [GearmanTask::jobHandle()](gearmantask.jobhandle.md) \- Отримати дескриптор завдання
