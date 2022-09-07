---
navigation:
  - event.settimer.md: '« Event::setTimer'
  - event.timer.md: 'Event::timer »'
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::signal'
---
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

Створює об'єкт події сигналу. Це полегшений метод створення події сигналу. Зверніть увагу, що штатний конструктор [Event::construct()](event.construct.md) може також створювати події сигналу.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`signum`

Номер сигналу.

`cb`

Функція зворотного дзвінка події сигналу. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.md)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event. У разі виникнення помилки повертає **`false`**

### Дивіться також

-   [Створення подій сигналу](event.constructing.signal.events.md)
