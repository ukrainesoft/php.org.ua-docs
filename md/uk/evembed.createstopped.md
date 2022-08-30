Створює зупинений об'єкт спостерігач EvEmbed

-   [« EvEmbed::construct](evembed.construct.md)
    
-   [EvEmbed::set »](evembed.set.md)
    
-   [PHP Manual](index.md)
    
-   [EvEmbed](class.evembed.md)
    
-   Створює зупинений об'єкт спостерігач EvEmbed
    

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

Те саме, що й [EvEmbed::construct()](evembed.construct.md) , але спостерігача не буде автоматично запущено.

### Список параметрів

`other`

Те саме, що і для [EvEmbed::construct()](evembed.construct.md)

`callback`

Дивіться [callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Дані користувача, асоційовані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає зупинений спостерігач EvEmbed.

### Дивіться також

-   [EvEmbed::construct()](evembed.construct.md) - Конструктор об'єкту EvEmbed
-   [Ev::embeddableBackends()](ev.embeddablebackends.md) - Повертає набір бекендів, які можна вбудувати в інші цикли подій