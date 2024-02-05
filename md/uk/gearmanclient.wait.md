---
navigation:
  - gearmanclient.timeout.md: '« GearmanClient::timeout'
  - class.gearmanjob.md: GearmanJob »
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::wait'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::wait

(PECL gearman >= 0.6.0)

GearmanClient::wait — Очікує активності вводу-виводу для всіх підключень на клієнта

### Опис

```methodsynopsis
public GearmanClient::wait(): bool
```

Чекає на активність від будь-якого з підключених серверів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`** у разі успішного виконання, \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanWorker::wait()](gearmanworker.wait.md) \- Очікування запиту з одного із сервера завдань
