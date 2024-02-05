---
navigation:
  - hrtime-stopwatch.getlastelapsedticks.md: '« HRTime\\StopWatch::getLastElapsedTicks'
  - hrtime-stopwatch.isrunning.md: 'HRTime\\StopWatch::isRunning »'
  - index.md: PHP Manual
  - class.hrtime-stopwatch.md: HRTime\\StopWatch
title: 'HRTime\\StopWatch::getLastElapsedTime'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# HRTime\\StopWatch::getLastElapsedTime

(PECL hrtime >= 0.4.3)

HRTime\\StopWatch::getLastElapsedTime — Отримати минулий час для останнього інтервалу

### Опис

```methodsynopsis
public HRTime\StopWatch::getLastElapsedTime(int $unit = ?): float
```

Повертає час для раніше закритого інтервалу.

### Список параметрів

`unit`

Одиниця часу, задана однією із констант HRTime\\Unit. Типово HRTime\\Unit::SECOND.

### Значення, що повертаються

Повертає значення типу float, що дорівнює минулому часу.
