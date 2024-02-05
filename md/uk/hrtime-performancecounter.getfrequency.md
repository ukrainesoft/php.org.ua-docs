---
navigation:
  - class.hrtime-performancecounter.md: « HRTime\\PerformanceCounter
  - hrtime-performancecounter.getticks.md: 'HRTime\\PerformanceCounter::getTicks »'
  - index.md: PHP Manual
  - class.hrtime-performancecounter.md: HRTime\\PerformanceCounter
title: 'HRTime\\PerformanceCounter::getFrequency'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# HRTime\\PerformanceCounter::getFrequency

(PECL hrtime >= 0.4.3)

HRTime\\PerformanceCounter::getFrequency — Частота таймера в тиках за секунду

### Опис

```methodsynopsis
public static HRTime\PerformanceCounter::getFrequency(): int
```

Повертає частоту таймера в тиках за секунду. Це буде постійним значенням після старту системи більшості операційних систем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число (int), що дорівнює частоті таймера.
