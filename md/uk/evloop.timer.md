---
navigation:
  - evloop.suspend.md: '« EvLoop::suspend'
  - evloop.verify.md: 'EvLoop::verify »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::timer'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::timer

(PECL ev >= 0.2.0)

EvLoop::timer — Створює об'єкт спостерігача EvTimer, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::timer(    
    float
     $after
   ,    
    float
     $repeat
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
   ): EvTimer
```

Створює об'єкт спостерігача EvTimer, пов'язаний із поточним екземпляром циклу подій.

### Список параметрів

Усі параметри, що й для [EvTimer::\_\_construct()](evtimer.construct.md)

### Значення, що повертаються

Повертає об'єкт EvTimer у разі успішного виконання.

### Дивіться також

-   [EvTimer::\_\_construct()](evtimer.construct.md) \- Конструктор об'єкта спостерігача EvTimer
