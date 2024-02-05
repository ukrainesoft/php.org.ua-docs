---
navigation:
  - evembed.construct.md: '« EvEmbed::\_\_construct'
  - evembed.set.md: 'EvEmbed::set »'
  - index.md: PHP Manual
  - class.evembed.md: EvEmbed
title: 'EvEmbed::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvEmbed::createStopped

(PECL ev >= 0.2.0)

EvEmbed::createStopped — Створює зупинений об'єкт спостерігач EvEmbed

### Опис

```methodsynopsis
final
   public
   static
   EvEmbed::createStopped(    
    object
     $other
   ,    
    callable
     $callback
    = ?,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?): void
```

Те саме, що й [EvEmbed::\_\_construct()](evembed.construct.md) , але спостерігача не буде автоматично запущено.

### Список параметрів

`other`

Те саме, що і для [EvEmbed::\_\_construct()](evembed.construct.md)

`callback`

Смотрите[callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Дані користувача, асоційовані з спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає зупинений спостерігач EvEmbed.

### Дивіться також

-   [EvEmbed::\_\_construct()](evembed.construct.md) \- Конструктор об'єкту EvEmbed
-   [Ev::embeddableBackends()](ev.embeddablebackends.md) \- Повертає набір бекендів, які можна вбудувати в інші цикли подій
