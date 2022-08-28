Конструктор спостерігача EvIdle

-   [« EvIdle](class.evidle.html)
    
-   [EvIdle::createStopped »](evidle.createstopped.html)
    
-   [PHP Manual](index.html)
    
-   [EvIdle](class.evidle.html)
    
-   Конструктор спостерігача EvIdle
    

# EvIdle::construct

(PECL ev >= 0.2.0)

EvIdle::construct - Конструктор спостерігача EvIdle

### Опис

public **EvIdle::construct** [callable](language.types.callable.html) `$callback` [mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` ?, int `$priority`

Створює об'єкт спостерігач EvIdle та автоматично його стартує.

### Список параметрів

`callback`

Дивіться [функции обратного вызова наблюдателей](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvIdle::createStopped()](evidle.createstopped.html) - Створити об'єкт класу EvIdle, але не стартувати його
-   [EvLoop::idle()](evloop.idle.html) - Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій