---
navigation:
  - evloop.stop.html: '« EvLoop::stop'
  - evloop.timer.html: 'EvLoop::timer »'
  - index.html: PHP Manual
  - class.evloop.html: EvLoop
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

Методи **EvLoop::suspend()** і [EvLoop::resume()](evloop.resume.html) зупиняють та відновлюють цикл відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::resume()](evloop.resume.html) - Відновлює раніше зупинений цикл подій
-   [Ev::suspend()](ev.suspend.html) - Зупинити подійний цикл за замовчуванням
