Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::signal](evloop.signal.html)
    
-   [EvLoop::stop »](evloop.stop.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::stat

(PECL ev >= 0.2.0)

EvLoop::stat — Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::stat(    
    string
     $path
   ,    
    float
     $interval
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
   ): EvStat
```

Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій.

### Список параметрів

Усі параметри, що й для [EvSignal::construct()](evsignal.construct.html)

### Значення, що повертаються

Повертає об'єкт EvStat у разі успішного виконання

### Дивіться також

-   [EvSignal::construct()](evsignal.construct.html) - Конструктор об'єкта спостерігача EvSignal