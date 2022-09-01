---
navigation:
  - event.signal.md: '« Event::signal'
  - class.eventbase.md: EventBase »
  - index.md: PHP Manual
  - class.event.md: Event
title: 'Event::timer'
---
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

Створює об'єкт таймера. Це полегшений метод створення події сигналу. Зверніть увагу, що штатний конструктор [Event::construct()](event.construct.md) може також створювати події таймера.

### Список параметрів

`base`

Подієва база, до якої необхідно прив'язати подію.

`cb`

Функція зворотного дзвінка події таймера. Дивіться [Функції зворотного дзвінка для подій](event.callbacks.md)

`arg`

Ці дані, пов'язані з подією. Вони будуть передані у функцію зворотного виклику, коли відбудеться подія.

### Значення, що повертаються

Повертає об'єкт Event. У разі виникнення помилки повертає **`false`**
