---
navigation:
  - evperiodic.createstopped.html: '« EvPeriodic::createStopped'
  - class.evprepare.html: EvPrepare »
  - index.html: PHP Manual
  - class.evperiodic.html: EvPeriodic
title: 'EvPeriodic::set'
---
# EvPeriodic::set

(PECL ev >= 0.2.0)

EvPeriodic::set — Налаштовує спостерігача

### Опис

```methodsynopsis
public
   EvPeriodic::set(
    float
     $offset
   , 
    float
     $interval
   ): void
```

Налаштовує чи переналаштовує EvPeriodic спостерігача.

### Список параметрів

`offset`

Те саме, що і для [EvPeriodic::construct()](evperiodic.construct.html) . Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.html)

`interval`

Те саме, що і для [EvPeriodic::construct()](evperiodic.construct.html) . Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.html)

### Значення, що повертаються

Функція не повертає значення після виконання.
