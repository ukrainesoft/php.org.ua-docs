---
navigation:
  - evloop.check.md: '« EvLoop::check'
  - evloop.construct.md: 'EvLoop::\_\_construct »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::child'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::child

(PECL ev >= 0.2.0)

EvLoop::child — Створює об'єкт EvChild, пов'язаний із поточним циклом подій

### Опис

```methodsynopsis
final
   public
   EvLoop::child(    
    string
     $pid
   ,    
    string
     $trace
   ,    
    string
     $callback
   ,    
    string
     $data
    = ?,    
    string
     $priority
    = ?): EvChild
```

Створює об'єкт EvChild, пов'язаний із поточним циклом подій.

### Список параметрів

Усі параметри, що й для [EvChild::\_\_construct()](evchild.construct.md)

### Значення, що повертаються

Повертає об'єкт EvChild у разі успішного виконання.

### Дивіться також

-   [EvChild::\_\_construct()](evchild.construct.md) \- Створює об'єкт спостерігач EvChild
