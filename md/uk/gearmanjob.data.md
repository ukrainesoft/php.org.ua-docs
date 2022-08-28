Надсилання даних (застарілий метод)

-   [« GearmanJob::\_\_construct](gearmanjob.construct.html)
    
-   [GearmanJob::exception »](gearmanjob.exception.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання даних (застарілий метод)
    

# GearmanJob::data

(PECL gearman <= 0.5.0)

GearmanJob::data — Надсилання даних (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::data(string $data): bool
```

Відправляє дані серверу завдань (і всім клієнтам, що слухають).

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendData()](gearmanjob.senddata.html) у випуску 0.6.0 модуля Gearman.

### Список параметрів

`data`

Серіалізовані дані.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::workload()](gearmanjob.workload.html) - отримання даних для обробки
-   [GearmanTask::data()](gearmantask.data.html) - Отримати дані, повернені для завдання