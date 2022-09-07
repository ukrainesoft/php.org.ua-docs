---
navigation:
  - evchild.construct.md: '« EvChild::construct'
  - evchild.set.md: 'EvChild::set »'
  - index.md: PHP Manual
  - class.evchild.md: EvChild
title: 'EvChild::createStopped'
---
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

Те саме, що й [EvChild::construct()](evchild.construct.md) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`pid`

Дивіться [EvChild::construct()](evchild.construct.md)

`trace`

Дивіться [EvChild::construct()](evchild.construct.md)

`callback`

Дивіться [Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

### Дивіться також

-   [EvChild::construct()](evchild.construct.md) - Створює об'єкт спостерігач EvChild
-   [EvLoop::child()](evloop.child.md) - Створює об'єкт EvChild, пов'язаний із поточним циклом подій
