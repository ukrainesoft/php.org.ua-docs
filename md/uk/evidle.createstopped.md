---
navigation:
  - evidle.construct.md: '« EvIdle::construct'
  - class.evio.md: EvIo »
  - index.md: PHP Manual
  - class.evidle.md: EvIdle
title: 'EvIdle::createStopped'
---
# EvIdle::createStopped

(PECL ev >= 0.2.0)

EvIdle::createStopped — Створити об'єкт класу EvIdle, але не стартувати його

### Опис

```methodsynopsis
final
   public
   static
   EvIdle::createStopped(
    string
     $callback
   , 
    mixed
     $data
    = ?, 
    int
     $priority
    = ?): object
```

Те саме, що й [EvIdle::construct()](evidle.construct.md) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Дивіться [функції зворотного виклику спостерігачів](ev.watcher-callbacks.html)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvIdle.

### Дивіться також

-   [EvIdle::construct()](evidle.construct.md) - Конструктор спостерігача EvIdle
-   [EvLoop::idle()](evloop.idle.md) - Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій
