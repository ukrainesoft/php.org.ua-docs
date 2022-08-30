Створює зупинений екземпляр спостерігача EvCheck

-   [« EvCheck::construct](evcheck.construct.md)
    
-   [EvChild »](class.evchild.md)
    
-   [PHP Manual](index.md)
    
-   [EvCheck](class.evcheck.md)
    
-   Створює зупинений екземпляр спостерігача EvCheck
    

# EvCheck::createStopped

(PECL ev >= 0.2.0)

EvCheck::createStopped — Створює зупинений екземпляр спостерігача EvCheck

### Опис

```methodsynopsis
final
   public
   static
   EvCheck::createStopped(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): object
```

Створює зупинений екземпляр спостерігача EvCheck.

### Список параметрів

`callback`

Дивіться [Callback-функції спостерігача](ev.watcher-callbacks.html)

`data`

Дані, пов'язані зі спостерігачем.

`priority`

[приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає об'єкт EvCheck.

### Дивіться також

-   [EvPrepare](class.evprepare.md)