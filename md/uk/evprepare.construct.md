---
navigation:
  - class.evprepare.md: « EvPrepare
  - evprepare.createstopped.md: 'EvPrepare::createStopped »'
  - index.md: PHP Manual
  - class.evprepare.md: EvPrepare
title: 'EvPrepare::construct'
---
# EvPrepare::construct

(PECL ev >= 0.2.0)

EvPrepare::construct - Конструктор спостерігача EvPrepare

### Опис

public **EvPrepare::construct**(string `$callback` , string `$data` ?, string `$priority`

Створює об'єкт спостерігач EvPrepare та автоматично його стартує.

### Список параметрів

`callback`

Дивіться [функції зворотного виклику спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, асоційовані із спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.md#ev.constants.watcher-pri)

### Дивіться також

-   [EvCheck](class.evcheck.md)
