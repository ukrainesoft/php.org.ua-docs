---
navigation:
  - evloop.prepare.md: '« EvLoop::prepare'
  - evloop.run.md: 'EvLoop::run »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::resume'
---
# EvLoop::resume

(PECL ev >= 0.2.0)

EvLoop::resume — Відновлює раніше призупинений цикл подій

### Опис

```methodsynopsis
public
   EvLoop::resume(): void
```

Методи [EvLoop::suspend()](evloop.suspend.md) і **EvLoop::resume()** зупиняють та відновлюють цикл відповідно.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EvLoop::suspend()](evloop.suspend.md) - Припиняє цикл
-   [Ev::resume()](ev.resume.md) - Відновити виконання призупиненого раніше циклу подій за умовчанням
