Створює зупинений об'єкт спостерігач EvEmbed

-   [« EvEmbed::\_\_construct](evembed.construct.html)
    
-   [EvEmbed::set »](evembed.set.html)
    
-   [PHP Manual](index.html)
    
-   [EvEmbed](class.evembed.html)
    
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

Те саме, що й [EvEmbed::\_\_construct()](evembed.construct.html) , але спостерігача не буде автоматично запущено.

### Список параметрів

`other`

Те саме, що і для [EvEmbed::\_\_construct()](evembed.construct.html)

`callback`

Дивіться [callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Дані користувача, асоційовані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає зупинений спостерігач EvEmbed.

### Дивіться також

-   [EvEmbed::\_\_construct()](evembed.construct.html) - Конструктор об'єкту EvEmbed
-   [Ev::embeddableBackends()](ev.embeddablebackends.html) - Повертає набір бекендів, які можна вбудувати в інші цикли подій