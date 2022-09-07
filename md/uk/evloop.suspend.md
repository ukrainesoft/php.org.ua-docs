---
navigation:
  - evloop.stop.md: '« EvLoop::stop'
  - evloop.timer.md: 'EvLoop::timer »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::suspend'
---
# EvLoop::suspend

(PECL ev >= 0.2.0)

EvLoop::suspend — Припиняє цикл

### Опис

```methodsynopsis
public
   EvLoop::suspend(): void
```

Методи **EvLoop::suspend()** і [EvLoop::resume()](evloop.resume.md) зупиняють та відновлюють цикл відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::resume()](evloop.resume.md) - Відновлює раніше зупинений цикл подій
-   [Ev::suspend()](ev.suspend.md) - Зупинити подійний цикл за замовчуванням
