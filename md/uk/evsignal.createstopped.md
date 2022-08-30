Create stopped EvSignal watcher об'єкт

-   [« EvSignal::construct](evsignal.construct.md)
    
-   [EvSignal::set »](evsignal.set.md)
    
-   [PHP Manual](index.md)
    
-   [EvSignal](class.evsignal.md)
    
-   Create stopped EvSignal watcher об'єкт
    

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

Створює зупинений об'єкт спостерігач EvSignal. На відміну від [EvSignal::construct()](evsignal.construct.md), цей метод не запускає створеного спостерігача

### Список параметрів

`signum`

Номер сигналу. Дивіться константи модуля *pcntl* та документацію з `signal(7)`

`callback`

Дивіться [Функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Дані користувача, асоційовані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає об'єкт EvSignal.

### Дивіться також

-   [EvWatcher::start()](evwatcher.start.md) - Запускає спостерігача
-   [EvSignal::construct()](evsignal.construct.md) - Конструктор об'єкта спостерігача EvSignal