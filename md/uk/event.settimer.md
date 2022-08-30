Переконфігурація події таймера

-   [« Event::setPriority](event.setpriority.md)
    
-   [Event::signal »](event.signal.md)
    
-   [PHP Manual](index.md)
    
-   [Event](class.event.md)
    
-   Переконфігурація події таймера
    

# Event::setTimer

(PECL event >= 1.2.6-beta)

Event::setTimer — Переконфігурація події таймера

### Опис

```methodsynopsis
public
   Event::setTimer(
    EventBase
     $base
   , 
    callable
     $cb
   , 
    mixed
     $arg
    = ?): bool
```

Переконфігурує подію таймера. Зверніть увагу, що ця функція не викликає застарілої функції `event_set` бібліотеки libevent. Натомість вона викликає `event_assign`

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`cb`

Функція зворотного дзвінка події таймера. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.md)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [Event::construct()](event.construct.md) - Конструктор об'єкту Event
-   [Event::timer()](event.timer.md) - Створити об'єкт події таймера