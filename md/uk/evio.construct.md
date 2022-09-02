---
navigation:
  - class.evio.md: « EvIo
  - evio.createstopped.md: 'EvIo::createStopped »'
  - index.md: PHP Manual
  - class.evio.md: EvIo
title: 'EvIo::construct'
---
# EvIo::construct

(PECL ev >= 0.2.0)

EvIo::construct — Створює спостерігач об'єкт EvIo

### Опис

public **EvIo::construct**  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$fd`  
int `$events`  
[callable](language.types.callable.md) `$callback`  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data`  
int `$priority`

Створює та автоматично стартує об'єкт спостерігач EvIo.

### Список параметрів

`fd`

Може бути потоком, відкритим за допомогою функції [fopen()](function.fopen.md) чи аналогічною, числовим дескриптором файлу чи сокетом.

`events`

**`Ev::READ`** та/або **`Ev::WRITE`**. Дивіться [бітові маски](class.ev.md#ev.constants.watcher-revents)

`callback`

Дивіться [Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Приоритет наблюдателя](class.ev.md#ev.constants.watcher-pri)

### Дивіться також

-   [EvIo::createStopped()](evio.createstopped.md) - Створює зупинений об'єкт спостерігача EvIo
-   [EvLoop::io()](evloop.io.md) - Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій
