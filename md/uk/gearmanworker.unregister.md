---
navigation:
  - gearmanworker.timeout.md: '« GearmanWorker::timeout'
  - gearmanworker.unregisterall.md: 'GearmanWorker::unregisterAll »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::unregister'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::unregister

(PECL gearman >= 0.6.0)

GearmanWorker::unregister — Видалити реєстрацію імені функції на всіх серверах завдань

### Опис

```methodsynopsis
public GearmanWorker::unregister(string $function_name): bool
```

Знімає реєстрацію імені функції на всіх серверах завдань. Це означає, що цього оброблювача (цієї функції) завдання посилатися більше не будуть.

### Список параметрів

`function_name`

Ім'я функції, реєстрацію якої потрібно зняти.

### Значення, що повертаються

Стандартне значення, що повертається Gearman.

### Дивіться також

-   [GearmanWorker::register()](gearmanworker.register.md) \- Реєстрація функції на сервері завдань
-   [GearmanWorker::unregisterAll()](gearmanworker.unregisterall.md) \- Видалення реєстрації всіх імен функцій на серверах завдань
