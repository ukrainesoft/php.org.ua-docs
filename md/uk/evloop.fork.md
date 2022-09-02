---
navigation:
  - evloop.embed.md: '« EvLoop::embed'
  - evloop.idle.md: 'EvLoop::idle »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::fork'
---
# EvLoop::fork

(PECL ev >= 0.2.0)

EvLoop::fork — Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::fork(
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
   ): EvFork
```

Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для [EvFork::construct()](evfork.construct.md)

### Значення, що повертаються

Повертає об'єкт EvFork у разі успішного виконання.

### Дивіться також

-   [EvFork::construct()](evfork.construct.md) - Конструктор спостерігача EvFork
