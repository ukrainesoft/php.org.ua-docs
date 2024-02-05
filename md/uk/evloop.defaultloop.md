---
navigation:
  - evloop.construct.md: '« EvLoop::\_\_construct'
  - evloop.embed.md: 'EvLoop::embed »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::defaultLoop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::defaultLoop

(PECL ev >= 0.2.0)

EvLoop::defaultLoop — Повертає або створює цикл подій за промовчанням

### Опис

```methodsynopsis
public
   static
   EvLoop::defaultLoop(    
    int
     $flags
     = Ev::FLAG_AUTO
   ,    
    mixed
     $data
     = NULL
   ,    
    float
     $io_interval
     = 0.
   ,    
    float
     $timeout_interval
     = 0.
   ): EvLoop
```

Якщо цикл стандартних подій не створено, **EvLoop::defaultLoop()** створює його із зазначеними параметрами. В іншому випадку він просто повертає об'єкт, який представляє раніше створений екземпляр, ігноруючи всі параметри.

### Список параметрів

`flags`

Один из[прапори циклу подій](class.ev.md#ev.constants.loop-flags)

`data`

Ці дані, пов'язані з циклом.

`io_collect_interval`

Смотрите[io\_interval](class.evloop.md#evloop.props.io-interval)

`timeout_collect_interval`

Смотрите[timeout\_interval](class.evloop.md#evloop.props.timeout-interval)

### Значення, що повертаються

Повертає об'єкт EvLoop у разі успішного виконання.

### Дивіться також

-   [EvLoop::\_\_construct()](evloop.construct.md) \- Конструктор об'єкта циклу подій
