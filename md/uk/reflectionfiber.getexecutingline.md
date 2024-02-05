---
navigation:
  - reflectionfiber.getexecutingfile.md: '« ReflectionFiber::getExecutingFile'
  - reflectionfiber.getfiber.md: 'ReflectionFiber::getFiber »'
  - index.md: PHP Manual
  - class.reflectionfiber.md: ReflectionFiber
title: 'ReflectionFiber::getExecutingLine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFiber::getExecutingLine

(PHP 8 >= 8.1.0)

ReflectionFiber::getExecutingLine — Отримує номер рядка поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getExecutingLine(): int
```

Повертає номер рядка поточної точки виконання у відбитому класі [Fiber](class.fiber.md). Якщо файбер не було запущено або завершено, видається помилка [Error](class.error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Номер рядка поточної точки виконання файбера.
