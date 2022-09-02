---
navigation:
  - ev.watchers.md: « Спостерігачі
  - ev.periodic-modes.md: Режими роботи періодичних спостерігачів »
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Watcher callbacks
---
# Watcher callbacks

Усі спостерігачі можуть бути або активними (очікувати повідомлення), або неактивними (зупиненими). Тільки активні спостерігачі можуть викликати свої callback-функції. Усі такі функції викликаються як мінімум із двома параметрами: `watcher` - спостерігач, та `revents` - бітова маска прийнятих подій.

Callback-функції спостерігачів передаються в конструктори спостерігачів (класи, що успадковують від [EvWatcher](class.evwatcher.md) [EvCheck::construct()](evcheck.construct.md) [EvChild::construct()](evchild.construct.md) і т.д.) Callback-функція спостерігача повинна відповідати наступному прототипу:

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

Примірник спостерігача (клас розширює [EvWatcher](class.evwatcher.md)

`revents`

[Прийняті спостерігачем події](class.ev.md#ev.constants.watcher-revents)

Кожен тип спостерігача має власний біт у `revents`, асоційований з ним, що дозволяє використовувати одну і ту ж callback-функцію для безлічі спостерігачів. Подієва маска називається після типу, тобто . [EvChild](class.evchild.md) (або [EvLoop::child()](evloop.child.md)) встановлює **`EV::CHILD`** [EvPrepare](class.evprepare.md) (або [EvLoop::prepare()](evloop.prepare.md)) встановлює **`Ev::PREPARE`** [EvPeriodic](class.evperiodic.md) (або [EvLoop::periodic()](evloop.periodic.md)) встановлює **`Ev::PERIODIC`** і так далі, за винятком для подій введення/виводу (які встановлюють обидва біти, та **`Ev::READ`** і **`Ev::WRITE`**
