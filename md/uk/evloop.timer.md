---
navigation:
  - evloop.suspend.html: '« EvLoop::suspend'
  - evloop.verify.html: 'EvLoop::verify »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
title: 'EvLoop::timer'
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

Усі параметри, що й для [EvTimer::construct()](evtimer.construct.html)

### Значення, що повертаються

Повертає об'єкт EvTimer у разі успішного виконання.

### Дивіться також

-   [EvTimer::construct()](evtimer.construct.html) - Конструктор об'єкта спостерігача EvTimer
