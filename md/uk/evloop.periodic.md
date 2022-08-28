Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::nowUpdate](evloop.nowupdate.html)
    
-   [EvLoop::prepare »](evloop.prepare.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::periodic

(PECL ev >= 0.2.0)

EvLoop::periodic — Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::periodic(    
    float
     $offset
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
   ): EvPeriodic
```

Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvPeriodic::\_\_construct()](evperiodic.construct.html)

### Значення, що повертаються

Повертає об'єкт EvPeriodic у разі успішного виконання.

### Дивіться також

-   [EvPeriodic::\_\_construct()](evperiodic.construct.html) - Конструктор об'єкта спостерігача EvPeriodic