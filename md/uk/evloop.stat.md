---
navigation:
  - evloop.signal.md: '« EvLoop::signal'
  - evloop.stop.md: 'EvLoop::stop »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::stat'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::stat

(PECL ev >= 0.2.0)

EvLoop::stat — Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::stat(    
    string
     $path
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
   ): EvStat
```

Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій.

### Список параметрів

Усі параметри, що й для [EvSignal::\_\_construct()](evsignal.construct.md)

### Значення, що повертаються

Повертає об'єкт EvStat у разі успішного виконання

### Дивіться також

-   [EvSignal::\_\_construct()](evsignal.construct.md) \- Конструктор об'єкта спостерігача EvSignal
