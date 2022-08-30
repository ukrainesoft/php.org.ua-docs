Створює об'єкт EvChild, пов'язаний із поточним циклом подій

-   [« EvLoop::check](evloop.check.md)
    
-   [EvLoop::construct »](evloop.construct.md)
    
-   [PHP Manual](index.md)
    
-   [EvLoop](class.evloop.md)
    
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

Усі параметри, що й для [EvChild::construct()](evchild.construct.md)

### Значення, що повертаються

Повертає об'єкт EvChild у разі успішного виконання.

### Дивіться також

-   [EvChild::construct()](evchild.construct.md) - Створює об'єкт спостерігач EvChild