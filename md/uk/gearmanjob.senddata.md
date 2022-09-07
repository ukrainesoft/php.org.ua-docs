---
navigation:
  - gearmanjob.sendcomplete.md: '« GearmanJob::sendComplete'
  - gearmanjob.sendexception.md: 'GearmanJob::sendException »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::sendData'
---
# GearmanJob::sendData

(PECL gearman >= 0.6.0)

GearmanJob::sendData — Надсилання даних завдання, що виконується.

### Опис

```methodsynopsis
public GearmanJob::sendData(string $data): bool
```

Відправляє дані серверу завдань (і всім клієнтам, що слухають).

### Список параметрів

`data`

Серіалізовані дані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::workload()](gearmanjob.workload.md) - отримання даних для обробки
-   [GearmanTask::data()](gearmantask.data.md) - Отримати дані, повернені для завдання
