Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::fork](evloop.fork.html)
    
-   [EvLoop::invokePending »](evloop.invokepending.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::idle

(PECL ev >= 0.2.0)

EvLoop::idle — Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::idle(
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
   ): EvIdle
```

Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvIdle::construct()](evidle.construct.html)

### Значення, що повертаються

Повертає об'єкт EvIdle у разі успішного виконання.

### Дивіться також

-   [EvIdle::construct()](evidle.construct.html) - Конструктор спостерігача EvIdle