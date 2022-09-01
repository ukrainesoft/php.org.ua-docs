---
navigation:
  - evloop.defaultloop.html: '« EvLoop::defaultLoop'
  - evloop.fork.html: 'EvLoop::fork »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
title: 'EvLoop::embed'
---
# EvLoop::embed

(PECL ev >= 0.2.0)

EvLoop::embed — Створює екземпляр спостерігача EvEmbed, пов'язаний із поточним об'єктом EvLoop

### Опис

```methodsynopsis
final
   public
   EvLoop::embed(    
    string
     $other
   ,    
    string
     $callback
    = ?,    
    string
     $data
    = ?,    
    string
     $priority
    = ?): EvEmbed
```

Створює екземпляр спостерігача [EvEmbed](class.evembed.html), пов'язаний із поточним об'єктом [EvLoop](class.evloop.html)

### Список параметрів

Усі параметри, що й для [EvEmbed::construct()](evembed.construct.html)

### Значення, що повертаються

Повертає об'єкт EvEmbed у разі успішного виконання.

### Дивіться також

-   [EvEmbed::construct()](evembed.construct.html) - Конструктор об'єкту EvEmbed
