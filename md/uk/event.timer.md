Створити об'єкт події таймера

-   [« Event::signal](event.signal.html)
    
-   [EventBase »](class.eventbase.html)
    
-   [PHP Manual](index.html)
    
-   [Event](class.event.html)
    
-   Створити об'єкт події таймера
    

# Event::timer

(PECL event >= 1.2.6-beta)

Event::timer — Створити об'єкт події таймера

### Опис

```methodsynopsis
public
   static
   Event::timer(
    EventBase
     $base
   , 
    callable
     $cb
   , 
    mixed
     $arg
    = ?): Event
```

Створює об'єкт таймера. Це полегшений метод створення події сигналу. Зверніть увагу, що штатний конструктор [Event::construct()](event.construct.html) може також створювати події таймера.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`cb`

Функція зворотного дзвінка події таймера. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.html)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event. У разі виникнення помилки повертає **`false`**