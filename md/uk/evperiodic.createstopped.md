---
navigation:
  - evperiodic.construct.html: '« EvPeriodic::construct'
  - evperiodic.set.html: 'EvPeriodic::set »'
  - index.html: PHP Manual
  - class.evperiodic.html: EvPeriodic
title: 'EvPeriodic::createStopped'
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

Створює зупинений спостерігач EvPeriodic. На відміну від [EvPeriodic::construct()](evperiodic.construct.md), цей метод не запускає спостерігача автоматично.

### Список параметрів

`offset`

Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`interval`

Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`reschedule_cb`

Перепризначити callback-функцію. Ви можете передати **`null`**. Дивіться [Періодичні режими роботи спостерігача](ev.periodic-modes.md)

`callback`

Дивіться [Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігачів](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає об'єкт спостерігача EvPeriodic у разі успішного виконання.

### Дивіться також

-   [EvPeriodic::construct()](evperiodic.construct.md) - Конструктор об'єкта спостерігача EvPeriodic
-   [EvTimer::createStopped()](evtimer.createstopped.md) - створює зупинений спостерігач EvTimer
