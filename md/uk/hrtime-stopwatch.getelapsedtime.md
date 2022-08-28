Отримати сумарний час всіх інтервалів

-   [« HRTime\\StopWatch::getElapsedTicks](hrtime-stopwatch.getelapsedticks.html)
    
-   [HRTime\\StopWatch::getLastElapsedTicks »](hrtime-stopwatch.getlastelapsedticks.html)
    
-   [PHP Manual](index.html)
    
-   [HRTime\\StopWatch](class.hrtime-stopwatch.html)
    
-   Отримати сумарний час всіх інтервалів
    

# HRTimeStopWatch::getElapsedTime

(PECL hrtime >= 0.4.3)

HRTimeStopWatch::getElapsedTime — Отримати сумарний час усіх інтервалів, що минув.

### Опис

```methodsynopsis
public HRTime\StopWatch::getElapsedTime(int $unit = ?): float
```

Повертає сумарний час усіх інтервалів.

### Список параметрів

`unit`

Одиниця часу, задана однією із констант HRTimeUnit. Типово HRTimeUnit::SECOND.

### Значення, що повертаються

Повертає значення типу float, що дорівнює минулому часу.