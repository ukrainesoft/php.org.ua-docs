---
navigation:
  - evidle.construct.md: '« EvIdle::\_\_construct'
  - class.evio.md: EvIo »
  - index.md: PHP Manual
  - class.evidle.md: EvIdle
title: 'EvIdle::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Те саме, що й [EvIdle::\_\_construct()](evidle.construct.md) але не виробляє автоматичного старту спостерігача.

### Список параметрів

`callback`

Смотрите[функції зворотного виклику спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

Повертає зупинений об'єкт EvIdle.

### Дивіться також

-   [EvIdle::\_\_construct()](evidle.construct.md) \- Конструктор спостерігача EvIdle
-   [EvLoop::idle()](evloop.idle.md) \- Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій
