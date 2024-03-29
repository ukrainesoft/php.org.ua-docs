---
navigation:
  - evloop.loopfork.md: '« EvLoop::loopFork'
  - evloop.nowupdate.md: 'EvLoop::nowUpdate »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::now'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::now

(PECL ev >= 0.2.0)

EvLoop::now — Повертає поточний "event loop time"

### Опис

```methodsynopsis
public
   EvLoop::now(): float
```

Повертає поточний "event loop time", тобто час, коли цикл подій отримав події та почав їх обробляти. Ця тимчасова мітка не змінюється, поки обробляються callback-функції, це також базовий час, який використовується для відносних таймерів. Ви можете розглядати його як мітку часу події (або, вірніше, коли libev дізнається про це).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає час циклу події у частках секунди.

### Дивіться також

-   [Ev::now()](ev.now.md) \- Отримати час запуску останньої ітерації циклу за замовчуванням
