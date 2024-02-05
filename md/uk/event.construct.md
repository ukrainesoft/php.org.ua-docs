---
navigation:
  - event.addtimer.md: '« Event::addTimer'
  - event.del.md: 'Event::del »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Event::\_\_construct

(PECL event >= 1.2.6-beta)

Event::\_\_construct - Конструктор об'єкта Event

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

База події, до якої необхідно прив'язати подію.

`fd`

Ресурс потоку, ресурс сокету чи числовий дескриптор файлу. Для подій таймера вказують **`-1`**. Для події сигналу задають його номер, наприклад **`SIGHUP`**

`what`

Прапори події. Докладніше про це розказано у розділі «[Прапори подій](event.flags.md)».

`cb`

Функція зворотного дзвінка. Докладніше про це розказано у розділі «[Функції зворотного дзвінка для подій](event.callbacks.md)».

`arg`

Ці дані, пов'язані з подією. Якщо задані, вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Дивіться також

-   [Event::signal()](event.signal.md) \- Створити об'єкт події сигналу
-   [Event::timer()](event.timer.md) \- Створити об'єкт події таймера
