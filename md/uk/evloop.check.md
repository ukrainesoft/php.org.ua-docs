---
navigation:
  - evloop.backend.html: '« EvLoop::backend'
  - evloop.child.html: 'EvLoop::child »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
title: 'EvLoop::check'
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

Усі параметри, що й для [EvCheck::construct()](evcheck.construct.html)

### Значення, що повертаються

Повертає об'єкт EvCheck у разі успішного виконання.

### Дивіться також

-   [EvCheck::construct()](evcheck.construct.html) - Конструктор об'єкту EvCheck
