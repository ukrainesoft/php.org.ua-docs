Створити об'єкт класу EvIdle, але не стартувати його

-   [« EvIdle::construct](evidle.construct.html)
    
-   [EvIo »](class.evio.html)
    
-   [PHP Manual](index.html)
    
-   [EvIdle](class.evidle.html)
    
-   Створити об'єкт класу EvIdle, але не стартувати його
    

# EvIdle::createStopped

(PECL ev >= 0.2.0)

EvIdle::createStopped — Створити об'єкт класу EvIdle, але не стартувати його

### Опис

```methodsynopsis
final
   public
   static
   EvIdle::createStopped(
    string
     $callback
   , 
    mixed
     $data
    = ?, 
    int
     $priority
    = ?): object
```

Те саме, що й [EvIdle::construct()](evidle.construct.html) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvIdle.

### Дивіться також

-   [EvIdle::construct()](evidle.construct.html) - Конструктор спостерігача EvIdle
-   [EvLoop::idle()](evloop.idle.html) - Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій