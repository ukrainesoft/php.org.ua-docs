---
navigation:
  - class.hrtime-performancecounter.md: « HRTimePerformanceCounter
  - hrtime-performancecounter.getticks.md: 'HRTimePerformanceCounter::getTicks »'
  - index.md: PHP Manual
  - class.hrtime-performancecounter.md: HRTimePerformanceCounter
title: 'HRTimePerformanceCounter::getFrequency'
---
# HRTimePerformanceCounter::getFrequency

(PECL hrtime >= 0.4.3)

HRTimePerformanceCounter::getFrequency — Частота таймера в тиках за секунду

### Опис

```methodsynopsis
public static HRTime\PerformanceCounter::getFrequency(): int
```

Повертає частоту таймера в тиках за секунду. Це буде постійним значенням після старту системи більшості операційних систем.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число (int), що дорівнює частоті таймера.
