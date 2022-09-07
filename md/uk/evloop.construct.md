---
navigation:
  - evloop.child.md: '« EvLoop::child'
  - evloop.defaultloop.md: 'EvLoop::defaultLoop »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::construct'
---
# EvLoop::construct

(PECL ev >= 0.2.0)

EvLoop::construct - Конструктор об'єкта циклу подій

### Опис

public **EvLoop::construct**  
int `$flags`  
[mixed](language.types.declarations.md#language.types.declarations.mixed) `$data` NULL,  
float `$io_interval`  
float `$timeout_interval`

Конструктор об'єкта циклу подій.

### Список параметрів

`flags`

Один з [прапори циклу подій](class.ev.md#ev.constants.loop-flags)

`data`

Ці дані, пов'язані з циклом.

`io_interval`

Дивіться [іоinterval](class.evloop.md#evloop.props.io-interval)

`timeout_interval`

Дивіться [timeoutinterval](class.evloop.md#evloop.props.timeout-interval)

### Дивіться також

-   [EvLoop::defaultLoop()](evloop.defaultloop.md) - Повертає або створює цикл подій за умовчанням
