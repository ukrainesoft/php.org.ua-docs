Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::embed](evloop.embed.html)
    
-   [EvLoop::idle »](evloop.idle.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::fork

(PECL ev >= 0.2.0)

EvLoop::fork — Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::fork(
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
   ): EvFork
```

Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvFork::\_\_construct()](evfork.construct.html)

### Значення, що повертаються

Повертає об'єкт EvFork у разі успішного виконання.

### Дивіться також

-   [EvFork::\_\_construct()](evfork.construct.html) - Конструктор спостерігача EvFork