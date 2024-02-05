---
navigation:
  - evloop.periodic.md: '« EvLoop::periodic'
  - evloop.resume.md: 'EvLoop::resume »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::prepare'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::prepare

(PECL ev >= 0.2.0)

EvLoop::prepare — Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::prepare(
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
   ): EvPrepare
```

Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій

### Список параметрів

Усі параметри, що й для **EvPrepare()**

### Значення, що повертаються

Повертає об'єкт EvPrepare у разі успішного виконання

### Дивіться також

-   [EvPrepare::\_\_construct()](evprepare.construct.md) \- Конструктор спостерігача EvPrepare
