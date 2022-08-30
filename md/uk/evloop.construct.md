Конструктор об'єкта циклу подій

-   [« EvLoop::child](evloop.child.md)
    
-   [EvLoop::defaultLoop »](evloop.defaultloop.md)
    
-   [PHP Manual](index.md)
    
-   [EvLoop](class.evloop.md)
    
-   Конструктор об'єкта циклу подій
    

# EvLoop::construct

(PECL ev >= 0.2.0)

EvLoop::construct - Конструктор об'єкта циклу подій

### Опис

public **EvLoop::construct**  
int `$flags`  
[mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` NULL,  
float `$io_interval`  
float `$timeout_interval`

Конструктор об'єкта циклу подій.

### Список параметрів

`flags`

Один з [прапори циклу подій](class.ev.html#ev.constants.loop-flags)

`data`

Ці дані, пов'язані з циклом.

`io_interval`

Дивіться [іоinterval](class.evloop.html#evloop.props.io-interval)

`timeout_interval`

Дивіться [timeoutinterval](class.evloop.html#evloop.props.timeout-interval)

### Дивіться також

-   [EvLoop::defaultLoop()](evloop.defaultloop.md) - Повертає або створює цикл подій за умовчанням