---
navigation:
  - hrtime-performancecounter.gettickssince.md: '« HRTime\\PerformanceCounter::getTicksSince'
  - hrtime-stopwatch.getelapsedticks.md: 'HRTime\\StopWatch::getElapsedTicks »'
  - index.md: PHP Manual
  - book.hrtime.md: HRTime
title: Клас HRTime\\StopWatch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас HRTime\\StopWatch

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

-   [HRTime\\StopWatch::getElapsedTicks](hrtime-stopwatch.getelapsedticks.md)— Отримати кількість тиків для всіх інтервалів.
-   [HRTime\\StopWatch::getElapsedTime](hrtime-stopwatch.getelapsedtime.md)— Отримати сумарний час усіх інтервалів, що минув.
-   [HRTime\\StopWatch::getLastElapsedTicks](hrtime-stopwatch.getlastelapsedticks.md)— Отримати кількість тиків, що пройшли, за останній інтервал
-   [HRTime\\StopWatch::getLastElapsedTime](hrtime-stopwatch.getlastelapsedtime.md)— Отримати минулий час для останнього інтервалу
-   [HRTime\\StopWatch::isRunning](hrtime-stopwatch.isrunning.md)— Перевірити, чи виконується вимір
-   [HRTime\\StopWatch::start](hrtime-stopwatch.start.md) \- Запустити вимір часу
-   [HRTime\\StopWatch::stop](hrtime-stopwatch.stop.md)— Зупинити вимір
