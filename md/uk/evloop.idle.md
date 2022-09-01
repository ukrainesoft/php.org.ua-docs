---
navigation:
  - evloop.fork.html: '« EvLoop::fork'
  - evloop.invokepending.html: 'EvLoop::invokePending »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
title: 'EvLoop::idle'
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

Усі параметри, що й для [EvIdle::construct()](evidle.construct.md)

### Значення, що повертаються

Повертає об'єкт EvIdle у разі успішного виконання.

### Дивіться також

-   [EvIdle::construct()](evidle.construct.md) - Конструктор спостерігача EvIdle
