Створює зупинений екземпляр спостерігача EvCheck

-   [« EvCheck::\_\_construct](evcheck.construct.html)
    
-   [EvChild »](class.evchild.html)
    
-   [PHP Manual](index.html)
    
-   [EvCheck](class.evcheck.html)
    
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

Дивіться [Callback-функции наблюдателя](ev.watcher-callbacks.html)

`data`

Дані, пов'язані зі спостерігачем.

`priority`

[приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання повертає об'єкт EvCheck.

### Дивіться також

-   [EvPrepare](class.evprepare.html)