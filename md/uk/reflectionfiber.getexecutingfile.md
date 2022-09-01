---
navigation:
  - reflectionfiber.getcallable.html: '« ReflectionFiber::getCallable'
  - reflectionfiber.getexecutingline.html: 'ReflectionFiber::getExecutingLine »'
  - index.html: PHP Manual
  - class.reflectionfiber.html: ReflectionFiber
title: 'ReflectionFiber::getExecutingFile'
---
# ReflectionFiber::getExecutingFile

(PHP 8> = 8.1.0)

ReflectionFiber::getExecutingFile — Отримує ім'я файлу поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getExecutingFile(): string
```

Повертає повний шлях та ім'я файлу поточної точки виконання у відображеному класі [Fiber](class.fiber.html). Якщо файбер не було запущено або завершено, видається помилка [Error](class.error.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повний шлях та ім'я файлу відбитого файбера.
