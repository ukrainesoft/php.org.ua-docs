Конструктор спостерігача EvIdle

-   [« EvIdle](class.evidle.md)
    
-   [EvIdle::createStopped »](evidle.createstopped.md)
    
-   [PHP Manual](index.md)
    
-   [EvIdle](class.evidle.md)
    
-   Конструктор спостерігача EvIdle
    

# EvIdle::construct

(PECL ev >= 0.2.0)

EvIdle::construct - Конструктор спостерігача EvIdle

### Опис

public **EvIdle::construct** [callable](language.types.callable.md) `$callback` [mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` ?, int `$priority`

Створює об'єкт спостерігач EvIdle та автоматично його стартує.

### Список параметрів

`callback`

Дивіться [функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvIdle::createStopped()](evidle.createstopped.md) - Створити об'єкт класу EvIdle, але не стартувати його
-   [EvLoop::idle()](evloop.idle.md) - Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій