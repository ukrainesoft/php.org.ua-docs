---
navigation:
  - evstat.construct.md: '« EvStat::\_\_construct'
  - evstat.prev.md: 'EvStat::prev »'
  - index.md: PHP Manual
  - class.evstat.md: EvStat
title: 'EvStat::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Створює об'єкт спостерігача EvStat, але не запускає його автоматично (на відміну від [EvStat::\_\_construct()](evstat.construct.md)

### Список параметрів

`path`

Шлях очікування зміни статусу.

`interval`

Підказує, як швидко очікується виявлення змін, та його зазвичай вказується **`0.0`**, щоб дозволити *libev* вибрати потрібне значення.

`callback`

Смотрите[Спостерігачі зворотного виклику](ev.watcher-callbacks.md)

`data`

Ці дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт спостерігача EvStat у разі успішного виконання.

### Дивіться також

-   [EvStat::\_\_construct()](evstat.construct.md) \- Створює об'єкт спостерігача EvStat
-   [EvWatcher::start()](evwatcher.start.md) \- Запускає спостерігача
