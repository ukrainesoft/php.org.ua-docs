Припиняє надсилання подій

-   [« EventBase::dispatch](eventbase.dispatch.html)
    
-   [EventBase::free »](eventbase.free.html)
    
-   [PHP Manual](index.html)
    
-   [EventBase](class.eventbase.html)
    
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

-   [EventBase::stop()](eventbase.stop.html) - Повідомляє eventbase припинити відправку подій