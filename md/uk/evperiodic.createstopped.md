---
navigation:
  - evperiodic.construct.md: '« EvPeriodic::\_\_construct'
  - evperiodic.set.md: 'EvPeriodic::set »'
  - index.md: PHP Manual
  - class.evperiodic.md: EvPeriodic
title: 'EvPeriodic::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvPeriodic::createStopped

(PECL ev >= 0.2.0)

EvPeriodic::createStopped — Створює зупинений спостерігач EvPeriodic

### Опис

```methodsynopsis
final
   public
   static
   EvPeriodic::createStopped(    
    float
     $offset
   ,    
    float
     $interval
   ,    
    callable
     $reschedule_cb
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   ): EvPeriodic
```

Створює зупинений спостерігач EvPeriodic. На відміну від [EvPeriodic::\_\_construct()](evperiodic.construct.md), цей метод не запускає спостерігача автоматично.

### Список параметрів

`offset`

Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`interval`

Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`reschedule_cb`

Перепризначити callback-функцію. Ви можете передати \*\*`null`\*\*Смотрите[Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`callback`

Смотрите[Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігачів](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає об'єкт спостерігача EvPeriodic у разі успішного виконання.

### Дивіться також

-   [EvPeriodic::\_\_construct()](evperiodic.construct.md) \- Конструктор об'єкта спостерігача EvPeriodic
-   [EvTimer::createStopped()](evtimer.createstopped.md) \- створює зупинений спостерігач EvTimer
