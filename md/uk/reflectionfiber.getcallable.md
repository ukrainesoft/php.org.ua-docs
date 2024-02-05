---
navigation:
  - reflectionfiber.construct.md: '« ReflectionFiber::\_\_construct'
  - reflectionfiber.getexecutingfile.md: 'ReflectionFiber::getExecutingFile »'
  - index.md: PHP Manual
  - class.reflectionfiber.md: ReflectionFiber
title: 'ReflectionFiber::getCallable'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFiber::getCallable

(PHP 8 >= 8.1.0)

ReflectionFiber::getCallable — Отримує об'єкт, що викликається, що використовується для створення файбера

### Опис

```methodsynopsis
public ReflectionFiber::getCallable(): callable
```

Повертає об'єкт, що використовується для створення [Fiber](class.fiber.md). Якщо файбер завершено, видається помилка [Error](class.error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає об'єкт, що використовується для створення [Fiber](class.fiber.md)
