---
navigation:
  - gearmanworker.unregister.md: '« GearmanWorker::unregister'
  - gearmanworker.wait.md: 'GearmanWorker::wait »'
  - index.md: PHP Manual
  - class.gearmanworker.md: GearmanWorker
title: 'GearmanWorker::unregisterAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanWorker::unregisterAll

(PECL gearman >= 0.6.0)

GearmanWorker::unregisterAll — Видалення реєстрації всіх імен функцій на серверах завдань

### Опис

```methodsynopsis
public GearmanWorker::unregisterAll(): bool
```

Знімає реєстрацію всіх зареєстрованих функцій на всіх серверах завдань. Це означає, що цьому обробнику більше не надходитиме жодних завдань.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Стандартне значення, що повертається Gearman.

### Дивіться також

-   [GearmanWorker::register()](gearmanworker.register.md) \- Реєстрація функції на сервері завдань
-   [GearmanWorker::unregister()](gearmanworker.unregister.md) \- Видалити реєстрацію імені функції на всіх серверах завдань
