Створює зупинений спостерігач EvPeriodic

-   [« EvPeriodic::\_\_construct](evperiodic.construct.html)
    
-   [EvPeriodic::set »](evperiodic.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvPeriodic](class.evperiodic.html)
    
-   Створює зупинений спостерігач EvPeriodic
    

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

Створює зупинений спостерігач EvPeriodic. На відміну від [EvPeriodic::\_\_construct()](evperiodic.construct.html), цей метод не запускає спостерігача автоматично.

### Список параметрів

`offset`

Дивіться [Периодические режимы работы наблюдателя](ev.periodic-modes.html)

`interval`

Дивіться [Периодические режимы работы наблюдателя](ev.periodic-modes.html)

`reschedule_cb`

Перепризначити callback-функцію. Ви можете передати **`null`**. Дивіться [Периодические режимы работы наблюдателя](ev.periodic-modes.html)

`callback`

Дивіться [Callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателей](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає об'єкт спостерігача EvPeriodic у разі успішного виконання.

### Дивіться також

-   [EvPeriodic::\_\_construct()](evperiodic.construct.html) - Конструктор об'єкта спостерігача EvPeriodic
-   [EvTimer::createStopped()](evtimer.createstopped.html) - створює зупинений спостерігач EvTimer