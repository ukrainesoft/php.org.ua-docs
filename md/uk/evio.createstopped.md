Створює зупинений об'єкт спостерігача EvIo

-   [« EvIo::\_\_construct](evio.construct.html)
    
-   [EvIo::set »](evio.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvIo](class.evio.html)
    
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

Те саме, що й [EvIo::\_\_construct()](evio.construct.html) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`fd`

Дивіться [EvIo::\_\_construct()](evio.construct.html)

`events`

Дивіться [EvIo::\_\_construct()](evio.construct.html)

`callback`

Дивіться [Callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання, повертає об'єкт EvIo.

### Дивіться також

-   [EvIo::\_\_construct()](evio.construct.html) - Створює об'єкт спостерігач EvIo
-   [EvLoop::io()](evloop.io.html) - Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій