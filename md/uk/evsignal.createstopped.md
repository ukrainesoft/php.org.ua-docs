Create stopped EvSignal watcher об'єкт

-   [« EvSignal::construct](evsignal.construct.html)
    
-   [EvSignal::set »](evsignal.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvSignal](class.evsignal.html)
    
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

Створює зупинений об'єкт спостерігач EvSignal. На відміну від [EvSignal::construct()](evsignal.construct.html), цей метод не запускає створеного спостерігача

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

-   [EvWatcher::start()](evwatcher.start.html) - Запускає спостерігача
-   [EvSignal::construct()](evsignal.construct.html) - Конструктор об'єкта спостерігача EvSignal