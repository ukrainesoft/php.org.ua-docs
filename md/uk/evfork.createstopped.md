Створити об'єкт класу EvFork, але не стартувати його

-   [« EvFork::construct](evfork.construct.md)
    
-   [EvIdle »](class.evidle.md)
    
-   [PHP Manual](index.md)
    
-   [EvFork](class.evfork.md)
    
-   Створити об'єкт класу EvFork, але не стартувати його
    

# EvFork::createStopped

(PECL ev >= 0.2.0)

EvFork::createStopped — Створити об'єкт класу EvFork, але не стартувати його

### Опис

```methodsynopsis
final
   public
   static
   EvFork::createStopped(
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

Те саме, що й [EvFork::construct()](evfork.construct.md) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [callback-функції спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvFork.

### Дивіться також

-   [EvFork::construct()](evfork.construct.md) - Конструктор спостерігача EvFork