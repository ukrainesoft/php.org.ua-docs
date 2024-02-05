---
navigation:
  - hrtime-stopwatch.getelapsedticks.md: '« HRTime\\StopWatch::getElapsedTicks'
  - hrtime-stopwatch.getlastelapsedticks.md: 'HRTime\\StopWatch::getLastElapsedTicks »'
  - index.md: PHP Manual
  - class.hrtime-stopwatch.md: HRTime\\StopWatch
title: 'HRTime\\StopWatch::getElapsedTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# HRTime\\StopWatch::getElapsedTime

(PECL hrtime >= 0.4.3)

HRTime\\StopWatch::getElapsedTime — Отримати сумарний час усіх інтервалів, що минув.

### Опис

```methodsynopsis
public HRTime\StopWatch::getElapsedTime(int $unit = ?): float
```

Повертає сумарний час усіх інтервалів.

### Список параметрів

`unit`

Одиниця часу, задана однією із констант HRTime\\Unit. Типово HRTime\\Unit::SECOND.

### Значення, що повертаються

Повертає значення типу float, що дорівнює минулому часу.
