---
navigation:
  - evloop.nowupdate.md: '« EvLoop::nowUpdate'
  - evloop.prepare.md: 'EvLoop::prepare »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::periodic'
---
# EvLoop::periodic

(PECL ev >= 0.2.0)

EvLoop::periodic — Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::periodic(    
    float
     $offset
   ,    
    float
     $interval
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
   ): EvPeriodic
```

Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvPeriodic::construct()](evperiodic.construct.md)

### Значення, що повертаються

Повертає об'єкт EvPeriodic у разі успішного виконання.

### Дивіться також

-   [EvPeriodic::construct()](evperiodic.construct.md) - Конструктор об'єкта спостерігача EvPeriodic
