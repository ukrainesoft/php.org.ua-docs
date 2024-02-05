---
navigation:
  - evchild.construct.md: '« EvChild::\_\_construct'
  - evchild.set.md: 'EvChild::set »'
  - index.md: PHP Manual
  - class.evchild.md: EvChild
title: 'EvChild::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Те саме, що й [EvChild::\_\_construct()](evchild.construct.md) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`pid`

Смотрите[EvChild::\_\_construct()](evchild.construct.md)

`trace`

Смотрите[EvChild::\_\_construct()](evchild.construct.md)

`callback`

Смотрите[Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

### Дивіться також

-   [EvChild::\_\_construct()](evchild.construct.md) \- Створює об'єкт спостерігач EvChild
-   [EvLoop::child()](evloop.child.md) \- Створює об'єкт EvChild, пов'язаний із поточним циклом подій
