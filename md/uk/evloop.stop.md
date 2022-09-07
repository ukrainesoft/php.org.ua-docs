---
navigation:
  - evloop.stat.md: '« EvLoop::stat'
  - evloop.suspend.md: 'EvLoop::suspend »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::stop'
---
# EvLoop::stop

(PECL ev >= 0.2.0)

EvLoop::stop — Зупиняє цикл подій

### Опис

```methodsynopsis
public
   EvLoop::stop(
    int
     $how
    = ?): void
```

Зупиняє цикл подій

### Список параметрів

`how`

Одна з *Ev::BREAK* [констант](class.ev.md#ev.constants.break-flags)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::run()](evloop.run.md) - Перевіряє події та викликає callback-функції в циклі
-   [Ev::stop()](ev.stop.md) - Зупинити подієвий цикл за замовчуванням
