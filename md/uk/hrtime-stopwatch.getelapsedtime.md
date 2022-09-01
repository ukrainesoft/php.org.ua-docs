---
navigation:
  - hrtime-stopwatch.getelapsedticks.html: '« HRTimeStopWatch::getElapsedTicks'
  - hrtime-stopwatch.getlastelapsedticks.html: 'HRTimeStopWatch::getLastElapsedTicks »'
  - index.md: PHP Manual
  - class.hrtime-stopwatch.html: HRTimeStopWatch
title: 'HRTimeStopWatch::getElapsedTime'
---
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
