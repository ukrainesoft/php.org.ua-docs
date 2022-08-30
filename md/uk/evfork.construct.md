Конструктор спостерігача EvFork

-   [« EvFork](class.evfork.html)
    
-   [EvFork::createStopped »](evfork.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvFork](class.evfork.html)
    
-   Конструктор спостерігача EvFork
    

# EvFork::construct

(PECL ev >= 0.2.0)

EvFork::construct - Конструктор спостерігача EvFork

### Опис

public **EvFork::construct** [callable](language.types.callable.html) `$callback` [mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` **`null`** , int `$priority`

Створює об'єкт спостерігач EvFork та автоматично його стартує.

### Список параметрів

`callback`

Дивіться [callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvLoop::fork()](evloop.fork.html) - Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій
-   [EvCheck](class.evcheck.html)