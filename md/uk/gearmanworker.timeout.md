Отримання значення час очікування запитів на сокеті

-   [« GearmanWorker::setTimeout](gearmanworker.settimeout.html)
    
-   [GearmanWorker::unregister »](gearmanworker.unregister.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanWorker](class.gearmanworker.html)
    
-   Отримання значення час очікування запитів на сокеті
    

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

-   [GearmanWorker::setTimeout()](gearmanworker.settimeout.html) - Завдання часу очікування на введення/виведення на сокеті