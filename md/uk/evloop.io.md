---
navigation:
  - evloop.invokepending.md: '« EvLoop::invokePending'
  - evloop.loopfork.md: 'EvLoop::loopFork »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::io'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::io

(PECL ev >= 0.2.0)

EvLoop::io — Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::io(    
    mixed
     $fd
   ,    
    int
     $events
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
   ): EvIo
```

Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvIo::\_\_construct()](evio.construct.md)

### Значення, що повертаються

Повертає об'єкт EvIo у разі успішного виконання.

### Дивіться також

-   [EvIo::\_\_construct()](evio.construct.md) \- Створює об'єкт спостерігач EvIo
