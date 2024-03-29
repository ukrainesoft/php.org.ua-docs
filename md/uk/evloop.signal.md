---
navigation:
  - evloop.run.md: '« EvLoop::run'
  - evloop.stat.md: 'EvLoop::stat »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::signal'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::signal

(PECL ev >= 0.2.0)

EvLoop::signal — Створює об'єкт спостерігача EvSignal, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::signal(    
    int
     $signum
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
   ): EvSignal
```

Створює об'єкт спостерігача EvSignal, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvSignal::\_\_construct()](evsignal.construct.md)

### Значення, що повертаються

Повертає об'єкт EvSignal у разі успішного виконання

### Дивіться також

-   [EvSignal::\_\_construct()](evsignal.construct.md) \- Конструктор об'єкта спостерігача EvSignal
