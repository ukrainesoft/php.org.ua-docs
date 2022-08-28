Видалення реєстрації всіх імен функцій на серверах завдань

-   [« GearmanWorker::unregister](gearmanworker.unregister.html)
    
-   [GearmanWorker::wait »](gearmanworker.wait.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanWorker](class.gearmanworker.html)
    
-   Видалення реєстрації всіх імен функцій на серверах завдань
    

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