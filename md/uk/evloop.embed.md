---
navigation:
  - evloop.defaultloop.md: '« EvLoop::defaultLoop'
  - evloop.fork.md: 'EvLoop::fork »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::embed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Створює екземпляр спостерігача [EvEmbed](class.evembed.md), пов'язаний із поточним об'єктом [EvLoop](class.evloop.md)

### Список параметрів

Усі параметри, що й для [EvEmbed::\_\_construct()](evembed.construct.md)

### Значення, що повертаються

Повертає об'єкт EvEmbed у разі успішного виконання.

### Дивіться також

-   [EvEmbed::\_\_construct()](evembed.construct.md) \- Конструктор об'єкту EvEmbed
