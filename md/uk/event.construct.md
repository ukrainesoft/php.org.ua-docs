Конструктор об'єкту Event

-   [« Event::addTimer](event.addtimer.md)
    
-   [Event::del »](event.del.md)
    
-   [PHP Manual](index.md)
    
-   [Event](class.event.md)
    
-   Конструктор об'єкту Event
    

# Event::construct

(PECL event >= 1.2.6-beta)

Event::construct - Конструктор об'єкта Event

### Опис

```methodsynopsis
public
   Event::__construct(    
    EventBase
     $base
   ,    
    mixed
     $fd
   ,    
    int
     $what
   ,    
    callable
     $cb
   ,    
    mixed
     $arg
     = NULL
   )
```

Створює об'єкт Event.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`fd`

Ресурс потоку, сокету чи числовий дескриптор файлу. Для подій таймера вкажіть **`-1`**. Для події сигналу задайте його номер, наприклад **`SIGHUP`**

`what`

Дивіться [Прапори подій](event.flags.md)

`cb`

Функція зворотного дзвінка. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.md)

`arg`

Ці дані, пов'язані з подією. Якщо задані, то вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event.

### Дивіться також

-   [Event::signal()](event.signal.md) - Створити об'єкт події сигналу
-   [Event::timer()](event.timer.md) - Створити об'єкт події таймера