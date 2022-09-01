---
navigation:
  - evprepare.construct.html: '« EvPrepare::construct'
  - class.evsignal.html: EvSignal »
  - index.html: PHP Manual
  - class.evprepare.html: EvPrepare
title: 'EvPrepare::createStopped'
---
# EvPrepare::createStopped

(PECL ev >= 0.2.0)

EvPrepare::createStopped — Створити об'єкт класу EvPrepare, але не стартувати його

### Опис

```methodsynopsis
final
   public
   static
   EvPrepare::createStopped(
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
   ): EvPrepare
```

Те саме, що й [EvPrepare::construct()](evprepare.construct.html) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvPrepare.

### Дивіться також

-   [EvPrepare::construct()](evprepare.construct.html) - Конструктор спостерігача EvPrepare
-   [EvWatcher::start()](evwatcher.start.html) - Запускає спостерігача
