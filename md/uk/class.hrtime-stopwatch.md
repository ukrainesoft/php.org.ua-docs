Клас HRTimeStopWatch

-   [« HRTimePerformanceCounter::getTicksSince](hrtime-performancecounter.gettickssince.html)
    
-   [HRTimeStopWatch::getElapsedTicks »](hrtime-stopwatch.getelapsedticks.html)
    
-   [PHP Manual](index.html)
    
-   [HRTime](book.hrtime.html)
    
-   Клас HRTimeStopWatch
    

# Клас HRTimeStopWatch

(PECL hrtime >= 0.4.3)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class HRTime\StopWatch
     

     
      extends
       HRTime\PerformanceCounter
     
     {
    

    /* Методы */
    
   public getElapsedTicks(): int
public getElapsedTime(int $unit = ?): float
public getLastElapsedTicks(): int
public getLastElapsedTime(int $unit = ?): float
public isRunning(): bool
public start(): void
public stop(): void


    /* Наследуемые методы */
    public static HRTime\PerformanceCounter::getFrequency(): int
public static HRTime\PerformanceCounter::getTicks(): int
public static HRTime\PerformanceCounter::getTicksSince(int $start): int


   }
```

## Зміст

-   [HRTimeStopWatch::getElapsedTicks](hrtime-stopwatch.getelapsedticks.html) — Отримати кількість тиків для всіх інтервалів.
-   [HRTimeStopWatch::getElapsedTime](hrtime-stopwatch.getelapsedtime.html) — Отримати сумарний час усіх інтервалів, що минув.
-   [HRTimeStopWatch::getLastElapsedTicks](hrtime-stopwatch.getlastelapsedticks.html) — Отримати кількість тиків, що пройшли, за останній інтервал
-   [HRTimeStopWatch::getLastElapsedTime](hrtime-stopwatch.getlastelapsedtime.html) — Отримати минулий час для останнього інтервалу
-   [HRTimeStopWatch::isRunning](hrtime-stopwatch.isrunning.html) — Перевірити, чи виконується вимір
-   [HRTimeStopWatch::start](hrtime-stopwatch.start.html) - Запустити вимір часу
-   [HRTimeStopWatch::stop](hrtime-stopwatch.stop.html) — Зупинити вимір