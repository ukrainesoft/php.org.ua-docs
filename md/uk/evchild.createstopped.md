Створює зупинений екземпляр спостерігача EvCheck

-   [« EvChild::construct](evchild.construct.html)
    
-   [EvChild::set »](evchild.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvChild](class.evchild.html)
    
-   Створює зупинений екземпляр спостерігача EvCheck
    

# EvChild::createStopped

(PECL ev >= 0.2.0)

EvChild::createStopped — Створює зупинений екземпляр спостерігача EvCheck

### Опис

```methodsynopsis
final
   public
   static
   EvChild::createStopped(    
    int
     $pid
   ,    
    bool
     $trace
   ,    
    callable
     $callback
   ,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?): object
```

Те саме, що й [EvChild::construct()](evchild.construct.html) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`pid`

Дивіться [EvChild::construct()](evchild.construct.html)

`trace`

Дивіться [EvChild::construct()](evchild.construct.html)

`callback`

Дивіться [Callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

### Дивіться також

-   [EvChild::construct()](evchild.construct.html) - Створює об'єкт спостерігач EvChild
-   [EvLoop::child()](evloop.child.html) - Створює об'єкт EvChild, пов'язаний із поточним циклом подій