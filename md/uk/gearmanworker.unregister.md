---
navigation:
  - gearmanworker.timeout.html: '« GearmanWorker::timeout'
  - gearmanworker.unregisterall.html: 'GearmanWorker::unregisterAll »'
  - index.html: PHP Manual
  - class.gearmanworker.html: GearmanWorker
title: 'GearmanWorker::unregister'
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

-   [GearmanWorker::register()](gearmanworker.register.html) - Реєстрація функції на сервері завдань
-   [GearmanWorker::unregisterAll()](gearmanworker.unregisterall.html) - Видалення реєстрації всіх імен функцій на серверах завдань
