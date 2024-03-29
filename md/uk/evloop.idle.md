---
navigation:
  - evloop.fork.md: '« EvLoop::fork'
  - evloop.invokepending.md: 'EvLoop::invokePending »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::idle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::idle

(PECL ev >= 0.2.0)

EvLoop::idle — Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::idle(
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
   ): EvIdle
```

Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvIdle::\_\_construct()](evidle.construct.md)

### Значення, що повертаються

Повертає об'єкт EvIdle у разі успішного виконання.

### Дивіться також

-   [EvIdle::\_\_construct()](evidle.construct.md) \- Конструктор спостерігача EvIdle
