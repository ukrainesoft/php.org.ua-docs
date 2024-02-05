---
navigation:
  - class.evidle.md: « EvIdle
  - evidle.createstopped.md: 'EvIdle::createStopped »'
  - index.md: PHP Manual
  - class.evidle.md: EvIdle
title: 'EvIdle::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvIdle::\_\_construct

(PECL ev >= 0.2.0)

EvIdle::\_\_construct - Конструктор спостерігача EvIdle

### Опис

public**EvIdle::\_\_construct** [callable](language.types.callable.md) `$callback` [mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` =?, int`$priority` =

Створює об'єкт спостерігач EvIdle та автоматично його стартує.

### Список параметрів

`callback`

Смотрите[функції зворотного виклику спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Дивіться також

-   [EvIdle::createStopped()](evidle.createstopped.md) \- Створити об'єкт класу EvIdle, але не стартувати його
-   [EvLoop::idle()](evloop.idle.md) \- Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій
