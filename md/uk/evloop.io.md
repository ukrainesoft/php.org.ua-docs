Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::invokePending](evloop.invokepending.html)
    
-   [EvLoop::loopFork »](evloop.loopfork.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::io

(PECL ev >= 0.2.0)

EvLoop::io — Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::io(    
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

Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvIo::\_\_construct()](evio.construct.html)

### Значення, що повертаються

Повертає об'єкт EvIo у разі успішного виконання.

### Дивіться також

-   [EvIo::\_\_construct()](evio.construct.html) - Створює об'єкт спостерігач EvIo