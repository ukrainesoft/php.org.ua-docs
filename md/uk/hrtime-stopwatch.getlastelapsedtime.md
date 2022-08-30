Отримати минулий час для останнього інтервалу

-   [« HRTimeStopWatch::getLastElapsedTicks](hrtime-stopwatch.getlastelapsedticks.html)
    
-   [HRTimeStopWatch::isRunning »](hrtime-stopwatch.isrunning.html)
    
-   [PHP Manual](index.html)
    
-   [HRTimeStopWatch](class.hrtime-stopwatch.html)
    
-   Отримати минулий час для останнього інтервалу
    

# HRTimeStopWatch::getLastElapsedTime

(PECL hrtime >= 0.4.3)

HRTimeStopWatch::getLastElapsedTime — Отримати минулий час для останнього інтервалу

### Опис

```methodsynopsis
public HRTime\StopWatch::getLastElapsedTime(int $unit = ?): float
```

Повертає час для раніше закритого інтервалу.

### Список параметрів

`unit`

Одиниця часу, задана однією із констант HRTimeUnit. Типово HRTimeUnit::SECOND.

### Значення, що повертаються

Повертає значення типу float, що дорівнює минулому часу.