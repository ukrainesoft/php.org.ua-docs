Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::periodic](evloop.periodic.html)
    
-   [EvLoop::resume »](evloop.resume.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::prepare

(PECL ev >= 0.2.0)

EvLoop::prepare — Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::prepare(
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
   ): EvPrepare
```

Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для **EvPrepare()**

### Значення, що повертаються

Повертає об'єкт EvPrepare у разі успішного виконання

### Дивіться також

-   [EvPrepare::\_\_construct()](evprepare.construct.html) - Конструктор спостерігача EvPrepare