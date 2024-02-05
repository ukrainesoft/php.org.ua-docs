---
navigation:
  - reflectionfiber.getcallable.md: '« ReflectionFiber::getCallable'
  - reflectionfiber.getexecutingline.md: 'ReflectionFiber::getExecutingLine »'
  - index.md: PHP Manual
  - class.reflectionfiber.md: ReflectionFiber
title: 'ReflectionFiber::getExecutingFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFiber::getExecutingFile

(PHP 8 >= 8.1.0)

ReflectionFiber::getExecutingFile — Отримує ім'я файлу поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getExecutingFile(): string
```

Повертає повний шлях та ім'я файлу поточної точки виконання у відображеному класі [Fiber](class.fiber.md). Якщо файбер не було запущено або завершено, видається помилка [Error](class.error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повний шлях та ім'я файлу відбитого файбера.
