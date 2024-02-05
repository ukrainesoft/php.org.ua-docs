---
navigation:
  - gearmanjob.construct.md: '« GearmanJob::\_\_construct'
  - gearmanjob.exception.md: 'GearmanJob::exception »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::data'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::data

(PECL gearman <= 0.5.0)

GearmanJob::data — Надсилання даних (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::data(string $data): bool
```

Відправляє дані серверу завдань (і всім клієнтам, що слухають).

> **Зауваження** :
> 
> Цей метод було замінено на [GearmanJob::sendData()](gearmanjob.senddata.md) у випуску 0.6.0 модуля Gearman.

### Список параметрів

`data`

Серіалізовані дані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [GearmanJob::workload()](gearmanjob.workload.md) \- отримання даних для обробки
-   [GearmanTask::data()](gearmantask.data.md) \- Отримати дані, повернені для завдання
