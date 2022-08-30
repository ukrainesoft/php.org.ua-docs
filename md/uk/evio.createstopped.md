Створює зупинений об'єкт спостерігача EvIo

-   [« EvIo::construct](evio.construct.md)
    
-   [EvIo::set »](evio.set.md)
    
-   [PHP Manual](index.md)
    
-   [EvIo](class.evio.md)
    
-   Створює зупинений об'єкт спостерігача EvIo
    

# EvIo::createStopped

(PECL ev >= 0.2.0)

EvIo::createStopped — Створює зупинений об'єкт спостерігача EvIo

### Опис

```methodsynopsis
final
   public
   static
   EvIo::createStopped(    
    mixed
     $fd
   ,    
    int
     $events
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
   ): EvIo
```

Те саме, що й [EvIo::construct()](evio.construct.md) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`fd`

Дивіться [EvIo::construct()](evio.construct.md)

`events`

Дивіться [EvIo::construct()](evio.construct.md)

`callback`

Дивіться [Callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання, повертає об'єкт EvIo.

### Дивіться також

-   [EvIo::construct()](evio.construct.md) - Створює об'єкт спостерігач EvIo
-   [EvLoop::io()](evloop.io.md) - Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій