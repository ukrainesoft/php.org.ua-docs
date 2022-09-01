---
navigation:
  - class.evcheck.html: « EvCheck
  - evcheck.createstopped.html: 'EvCheck::createStopped »'
  - index.html: PHP Manual
  - class.evcheck.html: EvCheck
title: 'EvCheck::construct'
---
# EvCheck::construct

(PECL ev >= 0.2.0)

EvCheck::construct — Конструктор об'єкту EvCheck

### Опис

public **EvCheck::construct** [callable](language.types.callable.md) `$callback` [mixed](language.types.declarations.html#language.types.declarations.mixed) `$data` ?, int `$priority`

Створює спостерігач [EvCheck](class.evcheck.md)

### Список параметрів

`callback`

Дивіться [Callback-функції спостерігача](ev.watcher-callbacks.md)

`data`

Дані, пов'язані зі спостерігачем.

`priority`

[приоритет наблюдателя](class.ev.html#ev.constants.watcher-pri)

### Дивіться також

-   [EvPrepare](class.evprepare.md)
-   [EvLoop::check()](evloop.check.md) - Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій
