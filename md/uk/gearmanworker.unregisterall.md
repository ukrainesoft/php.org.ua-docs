---
navigation:
  - gearmanworker.unregister.html: '« GearmanWorker::unregister'
  - gearmanworker.wait.html: 'GearmanWorker::wait »'
  - index.html: PHP Manual
  - class.gearmanworker.html: GearmanWorker
title: 'GearmanWorker::unregisterAll'
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

-   [GearmanWorker::register()](gearmanworker.register.html) - Реєстрація функції на сервері завдань
-   [GearmanWorker::unregister()](gearmanworker.unregister.html) - Видалити реєстрацію імені функції на всіх серверах завдань
