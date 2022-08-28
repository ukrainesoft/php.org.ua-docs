Конструктор об'єкту Event

-   [« Event::addTimer](event.addtimer.html)
    
-   [Event::del »](event.del.html)
    
-   [PHP Manual](index.html)
    
-   [Event](class.event.html)
    
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

Дивіться [Флаги событий](event.flags.html)

`cb`

Функція зворотного дзвінка. Дивіться [Функции обратного вызова для событий](event.callbacks.html)

`arg`

Ці дані, пов'язані з подією. Якщо задані, то вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event.

### Дивіться також

-   [Event::signal()](event.signal.html) - Створити об'єкт події сигналу
-   [Event::timer()](event.timer.html) - Створити об'єкт події таймера