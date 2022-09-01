---
navigation:
  - gearmanjob.sendcomplete.html: '« GearmanJob::sendComplete'
  - gearmanjob.sendexception.html: 'GearmanJob::sendException »'
  - index.html: PHP Manual
  - class.gearmanjob.html: GearmanJob
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

-   [GearmanJob::workload()](gearmanjob.workload.html) - отримання даних для обробки
-   [GearmanTask::data()](gearmantask.data.html) - Отримати дані, повернені для завдання
