---
navigation:
  - class.hrtime-performancecounter.html: « HRTimePerformanceCounter
  - hrtime-performancecounter.getticks.html: 'HRTimePerformanceCounter::getTicks »'
  - index.md: PHP Manual
  - class.hrtime-performancecounter.html: HRTimePerformanceCounter
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
