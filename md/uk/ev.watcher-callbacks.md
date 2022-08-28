Watcher callbacks

-   [« Наблюдатели](ev.watchers.html)
    
-   [Режимы работы периодических наблюдателей »](ev.periodic-modes.html)
    
-   [PHP Manual](index.html)
    
-   [Ev](book.ev.html)
    
-   Watcher callbacks
    

# Watcher callbacks

Усі спостерігачі можуть бути або активними (очікувати повідомлення), або неактивними (зупиненими). Тільки активні спостерігачі можуть викликати свої callback-функції. Усі такі функції викликаються як мінімум із двома параметрами: `watcher` - спостерігач, та `revents` - бітова маска прийнятих подій.

Callback-функції спостерігачів передаються в конструктори спостерігачів (класи, що успадковують від [EvWatcher](class.evwatcher.html) [EvCheck::\_\_construct()](evcheck.construct.html) [EvChild::\_\_construct()](evchild.construct.html) і т.д.) Callback-функція спостерігача повинна відповідати наступному прототипу:

```methodsynopsis
callback(
   object
    $watcher
    = NULL
  , 
   int
    $revents
    = NULL
  ): void
```

`watcher`

Примірник спостерігача (клас розширює [EvWatcher](class.evwatcher.html)

`revents`

[Принятые наблюдателем события](class.ev.html#ev.constants.watcher-revents)

Кожен тип спостерігача має власний біт у `revents`, асоційований з ним, що дозволяє використовувати одну і ту ж callback-функцію для безлічі спостерігачів. Подієва маска називається після типу, тобто . [EvChild](class.evchild.html) (або [EvLoop::child()](evloop.child.html)) встановлює **`EV::CHILD`** [EvPrepare](class.evprepare.html) (або [EvLoop::prepare()](evloop.prepare.html)) встановлює **`Ev::PREPARE`** [EvPeriodic](class.evperiodic.html) (або [EvLoop::periodic()](evloop.periodic.html)) встановлює **`Ev::PERIODIC`** і так далі, за винятком для подій введення/виводу (які встановлюють обидва біти, та **`Ev::READ`** і **`Ev::WRITE`**