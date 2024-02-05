---
navigation:
  - ev.watchers.md: « Спостерігачі
  - ev.periodic-modes.md: Режими роботи періодичних спостерігачів »
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Watcher callbacks
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Watcher callbacks

Усі спостерігачі можуть бути або активними (очікувати повідомлення), або неактивними (зупиненими). Тільки активні спостерігачі можуть викликати свої callback-функції. Усі такі функції викликаються як мінімум із двома параметрами: `watcher` - спостерігач, та `revents` - бітова маска прийнятих подій.

Callback-функції спостерігачів передаються в конструктори спостерігачів (класи, що успадковують від [EvWatcher](class.evwatcher.md) [EvCheck::\_\_construct()](evcheck.construct.md) [EvChild::\_\_construct()](evchild.construct.md)и т.д.) Callback-функция наблюдателя должна соответствовать следующему прототипу:

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

Кожен тип спостерігача має власний біт у `revents`, асоційований з ним, що дозволяє використовувати одну і ту ж callback-функцію для безлічі спостерігачів. Подієва маска називається після типу, тобто . [EvChild](class.evchild.md)(или[EvLoop::child()](evloop.child.md)) устанавливает\*\*`EV::CHILD`\*\* [EvPrepare](class.evprepare.md)(или[EvLoop::prepare()](evloop.prepare.md)) устанавливает\*\*`Ev::PREPARE`\*\* [EvPeriodic](class.evperiodic.md)(или[EvLoop::periodic()](evloop.periodic.md)) устанавливает\*\*`Ev::PERIODIC`\*\* і так далі, за винятком для подій введення/виводу (які встановлюють обидва біти, та **`Ev::READ`**и**`Ev::WRITE`**
