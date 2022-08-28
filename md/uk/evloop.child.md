Створює об'єкт EvChild, пов'язаний із поточним циклом подій

-   [« EvLoop::check](evloop.check.html)
    
-   [EvLoop::\_\_construct »](evloop.construct.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт EvChild, пов'язаний із поточним циклом подій
    

# EvLoop::child

(PECL ev >= 0.2.0)

EvLoop::child — Створює об'єкт EvChild, пов'язаний із поточним циклом подій

### Опис

```methodsynopsis
final
   public
   EvLoop::child(    
    string
     $pid
   ,    
    string
     $trace
   ,    
    string
     $callback
   ,    
    string
     $data
    = ?,    
    string
     $priority
    = ?): EvChild
```

Створює об'єкт EvChild, пов'язаний із поточним циклом подій.

### Список параметрів

Усі параметри, що й для [EvChild::\_\_construct()](evchild.construct.html)

### Значення, що повертаються

Повертає об'єкт EvChild у разі успішного виконання.

### Дивіться також

-   [EvChild::\_\_construct()](evchild.construct.html) - Створює об'єкт спостерігач EvChild