---
navigation:
  - gearmanjob.warning.html: '« GearmanJob::warning'
  - gearmanjob.workloadsize.html: 'GearmanJob::workloadSize »'
  - index.html: PHP Manual
  - class.gearmanjob.html: GearmanJob
title: 'GearmanJob::workload'
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

-   [GearmanClient::do()](gearmanclient.do.html) - Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanJob::workloadSize()](gearmanjob.workloadsize.html) - Отримання розміру даних, що оброблюються
