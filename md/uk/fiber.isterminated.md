---
navigation:
  - fiber.isrunning.md: '« Fiber::isRunning'
  - fiber.suspend.md: 'Fiber::suspend »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::isTerminated'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Fiber::isTerminated

(PHP 8 >= 8.1.0)

Fiber::isTerminated — Визначає, чи файбер завершено.

### Опис

```methodsynopsis
public Fiber::isTerminated(): bool
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** тільки після того, як файбер завершився, або шляхом повернення, або викинувши виняток, інакше повертає **`false`**
