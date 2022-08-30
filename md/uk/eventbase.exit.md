Припиняє надсилання подій

-   [« EventBase::dispatch](eventbase.dispatch.md)
    
-   [EventBase::free »](eventbase.free.md)
    
-   [PHP Manual](index.md)
    
-   [EventBase](class.eventbase.md)
    
-   Припиняє надсилання подій
    

# EventBase::exit

(PECL event >= 1.2.6-beta)

EventBase::exit — Припиняє надсилання подій

### Опис

```methodsynopsis
public
   EventBase::exit(
    float
     $timeout
    = ?): bool
```

Повідомляє, що база подій повинна припинити надсилання подій через вказану кількість секунд.

### Список параметрів

`timeout`

Необов'язковий параметр. Кількість секунд, після якого база подій повинна припинити надсилання подій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::stop()](eventbase.stop.md) - Повідомляє eventbase припинити відправку подій