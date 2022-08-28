Створити об'єкт класу EvFork, але не стартувати його

-   [« EvFork::\_\_construct](evfork.construct.html)
    
-   [EvIdle »](class.evidle.html)
    
-   [PHP Manual](index.html)
    
-   [EvFork](class.evfork.html)
    
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

Те саме, що й [EvFork::\_\_construct()](evfork.construct.html) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [callback-функции наблюдателей](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvFork.

### Дивіться також

-   [EvFork::\_\_construct()](evfork.construct.html) - Конструктор спостерігача EvFork