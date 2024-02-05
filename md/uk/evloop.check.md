---
navigation:
  - evloop.backend.md: '« EvLoop::backend'
  - evloop.child.md: 'EvLoop::child »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::check'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::check

(PECL ev >= 0.2.0)

EvLoop::check — Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій

### Опис

```methodsynopsis
final
   public
   EvLoop::check(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): EvCheck
```

Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій.

### Список параметрів

Усі параметри, що й для [EvCheck::\_\_construct()](evcheck.construct.md)

### Значення, що повертаються

Повертає об'єкт EvCheck у разі успішного виконання.

### Дивіться також

-   [EvCheck::\_\_construct()](evcheck.construct.md) \- Конструктор об'єкту EvCheck
