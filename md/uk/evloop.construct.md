---
navigation:
  - evloop.child.md: '« EvLoop::child'
  - evloop.defaultloop.md: 'EvLoop::defaultLoop »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::\_\_construct

(PECL ev >= 0.2.0)

EvLoop::\_\_construct - Конструктор об'єкта циклу подій

### Опис

public**EvLoop::\_\_construct**  
int`$flags` =  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` =NULL ,  
float`$io_interval` =  
float`$timeout_interval` =  
) .

Конструктор об'єкта циклу подій.

### Список параметрів

`flags`

Один из[прапори циклу подій](class.ev.md#ev.constants.loop-flags)

`data`

Ці дані, пов'язані з циклом.

`io_interval`

Смотрите[io\_interval](class.evloop.md#evloop.props.io-interval)

`timeout_interval`

Смотрите[timeout\_interval](class.evloop.md#evloop.props.timeout-interval)

### Дивіться також

-   [EvLoop::defaultLoop()](evloop.defaultloop.md) \- Повертає або створює цикл стандартних подій
