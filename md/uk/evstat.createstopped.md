Створює зупинений об'єкт спостерігача EvStat

-   [« EvStat::\_\_construct](evstat.construct.html)
    
-   [EvStat::prev »](evstat.prev.html)
    
-   [PHP Manual](index.html)
    
-   [EvStat](class.evstat.html)
    
-   Створює зупинений об'єкт спостерігача EvStat
    

# EvStat::createStopped

(PECL ev >= 0.2.0)

EvStat::createStopped — Створює зупинений об'єкт спостерігача EvStat

### Опис

```methodsynopsis
final
   public
   static
   EvStat::createStopped(    
    string
     $path
   ,    
    float
     $interval
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
   ): void
```

Створює об'єкт спостерігача EvStat, але не запускає його автоматично (на відміну від [EvStat::\_\_construct()](evstat.construct.html)

### Список параметрів

`path`

Шлях очікування зміни статусу.

`interval`

Підказує, як швидко очікується виявлення змін, та його зазвичай вказується **`0.0`**, щоб дозволити *libev* вибрати потрібне значення.

`callback`

Дивіться [Наблюдатели обратного вызова](ev.watcher-callbacks.html)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт спостерігача EvStat у разі успішного виконання.

### Дивіться також

-   [EvStat::\_\_construct()](evstat.construct.html) - Створює об'єкт спостерігача EvStat
-   [EvWatcher::start()](evwatcher.start.html) - Запускає спостерігача