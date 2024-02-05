---
navigation:
  - evperiodic.createstopped.md: '« EvPeriodic::createStopped'
  - class.evprepare.md: EvPrepare »
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Те саме, що і для [EvPeriodic::\_\_construct()](evperiodic.construct.md). Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`interval`

Те саме, що і для [EvPeriodic::\_\_construct()](evperiodic.construct.md). Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
