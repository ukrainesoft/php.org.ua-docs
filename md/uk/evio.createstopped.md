---
navigation:
  - evio.construct.md: '« EvIo::\_\_construct'
  - evio.set.md: 'EvIo::set »'
  - index.md: PHP Manual
  - class.evio.md: EvIo
title: 'EvIo::createStopped'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvIo::createStopped

(PECL ev >= 0.2.0)

EvIo::createStopped — Створює зупинений об'єкт спостерігача EvIo

### Опис

```methodsynopsis
final
   public
   static
   EvIo::createStopped(    
    mixed
     $fd
   ,    
    int
     $events
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   ): EvIo
```

Те саме, що й [EvIo::\_\_construct()](evio.construct.md) але не відбувається автоматичного запуску спостерігача.

### Список параметрів

`fd`

Смотрите[EvIo::\_\_construct()](evio.construct.md)

`events`

Смотрите[EvIo::\_\_construct()](evio.construct.md)

`callback`

Смотрите[Callback-функції спостерігачів](ev.watcher-callbacks.md)

`data`

Довільні дані, пов'язані зі спостерігачем.

`priority`

[Пріоритет спостерігача](class.ev.md#ev.constants.watcher-pri)

### Значення, що повертаються

У разі успішного виконання, повертає об'єкт EvIo.

### Дивіться також

-   [EvIo::\_\_construct()](evio.construct.md) \- Створює об'єкт спостерігач EvIo
-   [EvLoop::io()](evloop.io.md) \- Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій
