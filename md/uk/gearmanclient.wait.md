---
navigation:
  - gearmanclient.timeout.html: '« GearmanClient::timeout'
  - class.gearmanjob.html: GearmanJob »
  - index.html: PHP Manual
  - class.gearmanclient.html: GearmanClient
title: 'GearmanClient::wait'
---
# GearmanClient::wait

(PECL gearman >= 0.6.0)

GearmanClient::wait — Очікує активності введення-виводу для всіх підключень на клієнта

### Опис

```methodsynopsis
public GearmanClient::wait(): bool
```

Чекає на активність від будь-якого з підключених серверів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`** у разі успішного виконання, **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanWorker::wait()](gearmanworker.wait.html) - Очікування запиту з одного із сервера завдань
