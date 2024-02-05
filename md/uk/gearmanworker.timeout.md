---
navigation:
  - gearmanworker.settimeout.md: '« GearmanWorker::setTimeout'
  - gearmanworker.unregister.md: 'GearmanWorker::unregister »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::timeout'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::timeout

(PECL gearman >= 0.6.0)

GearmanWorker::timeout — Отримання значення час очікування запитів на сокеті

### Опис

```methodsynopsis
public GearmanWorker::timeout(): int
```

Повертає поточне значення часу очікування, тобто час, протягом якого обробник чекає на запит від сервера завдань.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Тимчасовий інтервал у мілісекундах. Негативне значення вказує на нескінченний час очікування.

### Дивіться також

-   [GearmanWorker::setTimeout()](gearmanworker.settimeout.md) \- Завдання часу очікування на введення/виведення на сокеті
