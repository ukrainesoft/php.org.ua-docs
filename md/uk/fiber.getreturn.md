---
navigation:
  - fiber.throw.md: '« Fiber::throw'
  - fiber.isstarted.md: 'Fiber::isStarted »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::getReturn'
---
# Fiber::getReturn

(PHP 8> = 8.1.0)

Fiber::getReturn — Отримує значення, яке повертається файбером

### Опис

```methodsynopsis
public Fiber::getReturn(): mixed
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає значення, що повертається [callable](language.types.callable.md)функцією, наданою в [Fiber::construct()](fiber.construct.md). Якщо файбер не повернув значення, або тому, що він не був запущений, або не був завершений, або викинув виняток, буде викинуто виняток [FiberError](class.fibererror.md)
