Повертає або створює цикл стандартних подій

-   [« EvLoop::construct](evloop.construct.html)
    
-   [EvLoop::embed »](evloop.embed.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Повертає або створює цикл стандартних подій
    

# EvLoop::defaultLoop

(PECL ev >= 0.2.0)

EvLoop::defaultLoop — Повертає або створює цикл подій за промовчанням

### Опис

```methodsynopsis
public
   static
   EvLoop::defaultLoop(    
    int
     $flags
     = Ev::FLAG_AUTO
   ,    
    mixed
     $data
     = NULL
   ,    
    float
     $io_interval
     = 0.
   ,    
    float
     $timeout_interval
     = 0.
   ): EvLoop
```

Якщо цикл стандартних подій не створено, **EvLoop::defaultLoop()** створює його із зазначеними параметрами. В іншому випадку він просто повертає об'єкт, який представляє раніше створений екземпляр, ігноруючи всі параметри.

### Список параметрів

`flags`

Один з [флагов цикла событий](class.ev.html#ev.constants.loop-flags)

`data`

Ці дані, пов'язані з циклом.

`io_collect_interval`

Дивіться [іоinterval](class.evloop.html#evloop.props.io-interval)

`timeout_collect_interval`

Дивіться [timeoutinterval](class.evloop.html#evloop.props.timeout-interval)

### Значення, що повертаються

Повертає об'єкт EvLoop у разі успішного виконання.

### Дивіться також

-   [EvLoop::construct()](evloop.construct.html) - Конструктор об'єкта циклу подій