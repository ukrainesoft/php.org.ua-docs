---
navigation:
  - evsignal.construct.md: '« EvSignal::\_\_construct'
  - evsignal.set.md: 'EvSignal::set »'
  - index.md: PHP Manual
  - class.evsignal.md: EvSignal
title: 'EvSignal::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvSignal::createStopped

(PECL ev >= 0.2.0)

EvSignal::createStopped — Create stopped EvSignal watcher object

### Опис

```methodsynopsis
final
   public
   static
   EvSignal::createStopped(    
    int
     $signum
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
   ): EvSignal
```

Створює зупинений об'єкт спостерігач EvSignal. На відміну від [EvSignal::\_\_construct()](evsignal.construct.md), цей метод не запускає створеного спостерігача

### Список параметрів

`signum`

Номер сигналу. Дивіться константи модуля *pcntl*и документацию по`signal(7)`

`callback`

Смотрите[Функції зворотного виклику спостерігачів](ev.watcher-callbacks.md)

`data`

Дані користувача, асоційовані з спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає об'єкт EvSignal.

### Дивіться також

-   [EvWatcher::start()](evwatcher.start.md) \- Запускає спостерігача
-   [EvSignal::\_\_construct()](evsignal.construct.md) \- Конструктор об'єкта спостерігача EvSignal
