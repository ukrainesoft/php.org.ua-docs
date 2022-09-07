---
navigation:
  - evperiodic.createstopped.md: '« EvPeriodic::createStopped'
  - class.evprepare.md: EvPrepare »
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
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

Те саме, що і для [EvPeriodic::construct()](evperiodic.construct.md) . Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`interval`

Те саме, що і для [EvPeriodic::construct()](evperiodic.construct.md) . Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
