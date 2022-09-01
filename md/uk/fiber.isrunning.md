---
navigation:
  - fiber.issuspended.md: '« Fiber::isSuspended'
  - fiber.isterminated.md: 'Fiber::isTerminated »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::isRunning'
---
# Fiber::isRunning

(PHP 8> = 8.1.0)

Fiber::isRunning — Визначає, чи працює файбер

### Опис

```methodsynopsis
public Fiber::isRunning(): bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** тільки якщо файбер працює. Файбер вважається працюючим після виклику [Fiber::start()](fiber.start.md) [Fiber::resume()](fiber.resume.md) або [Fiber::throw()](fiber.throw.md), який ще не повернуто. Повертає \*\*`false`\*\*якщо файбер не працює.
