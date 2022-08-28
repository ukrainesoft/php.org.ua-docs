Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій

-   [« EvLoop::backend](evloop.backend.html)
    
-   [EvLoop::child »](evloop.child.html)
    
-   [PHP Manual](index.html)
    
-   [EvLoop](class.evloop.html)
    
-   Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій
    

# EvLoop::check

(PECL ev >= 0.2.0)

EvLoop::check — Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::check(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): EvCheck
```

Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій.

### Список параметрів

Усі параметри, що й для [EvCheck::\_\_construct()](evcheck.construct.html)

### Значення, що повертаються

Повертає об'єкт EvCheck у разі успішного виконання.

### Дивіться також

-   [EvCheck::\_\_construct()](evcheck.construct.html) - Конструктор об'єкту EvCheck