---
navigation:
  - gearmanjob.warning.md: '« GearmanJob::warning'
  - gearmanjob.workloadsize.md: 'GearmanJob::workloadSize »'
  - index.md: PHP Manual
  - class.gearmanjob.md: GearmanJob
title: 'GearmanJob::workload'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanJob::workload

(PECL gearman >= 0.5.0)

GearmanJob::workload — Отримання даних для обробки

### Опис

```methodsynopsis
public GearmanJob::workload(): string
```

Повертає дані, передані для обробки. Це серіалізовані дані, з якими працюватиме обробник.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Серіалізовані дані.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.md) \- Виконує одне завдання та повертає результат\[Застарілий метод\]
-   [GearmanJob::workloadSize()](gearmanjob.workloadsize.md) \- Отримання розміру даних, що оброблюються
