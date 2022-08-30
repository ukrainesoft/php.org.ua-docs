Створити об'єкт події сигналу

-   [« Event::setTimer](event.settimer.html)
    
-   [Event::timer »](event.timer.html)
    
-   [PHP Manual](index.html)
    
-   [Event](class.event.html)
    
-   Створити об'єкт події сигналу
    

# Event::signal

(PECL event >= 1.2.6-beta)

Event::signal — Створити об'єкт події сигналу

### Опис

```methodsynopsis
public
   static
   Event::signal(    
    EventBase
     $base
   ,    
    int
     $signum
   ,    
    callable
     $cb
   ,    
    mixed
     $arg
    = ?): Event
```

Створює об'єкт події сигналу. Це полегшений метод створення події сигналу. Зверніть увагу, що штатний конструктор [Event::construct()](event.construct.html) може також створювати події сигналу.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`signum`

Номер сигналу.

`cb`

Функція зворотного дзвінка події сигналу. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.html)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event. У разі виникнення помилки повертає **`false`**

### Дивіться також

-   [Создание событий сигнала](event.constructing.signal.events.html)