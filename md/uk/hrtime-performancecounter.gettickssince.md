---
navigation:
  - hrtime-performancecounter.getticks.md: '« HRTimePerformanceCounter::getTicks'
  - class.hrtime-stopwatch.md: HRTimeStopWatch »
  - index.md: PHP Manual
  - class.hrtime-performancecounter.md: HRTimePerformanceCounter
title: 'HRTimePerformanceCounter::getTicksSince'
---
# HRTimePerformanceCounter::getTicksSince

(PECL hrtime >= 0.6.0)

HRTimePerformanceCounter::getTicksSince — Кількість тиків, що пройшли із заданого значення

### Опис

```methodsynopsis
public static HRTime\PerformanceCounter::getTicksSince(int $start): int
```

Повертає тиків, що пройшли із заданого початкового значення.

### Список параметрів

`start`

Початкове значення.

### Значення, що повертаються

Повертає ціле число (int), що дорівнює кількості тиків.
