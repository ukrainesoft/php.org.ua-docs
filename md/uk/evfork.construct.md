---
navigation:
  - class.evfork.md: « EvFork
  - evfork.createstopped.md: 'EvFork::createStopped »'
  - index.md: PHP Manual
  - class.evfork.md: EvFork
title: 'EvFork::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvFork::\_\_construct

(PECL ev >= 0.2.0)

EvFork::\_\_construct - Конструктор спостерігача EvFork

### Опис

public**EvFork::\_\_construct** [callable](language.types.callable.md) `$callback` [mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` = **`null`**, int`$priority` =

Створює об'єкт спостерігач EvFork та автоматично його стартує.

### Список параметрів

`callback`

Смотрите[callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Дивіться також

-   [EvLoop::fork()](evloop.fork.md) \- Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій
-   [EvCheck](class.evcheck.md)
