---
navigation:
  - class.fiber.md: « Fiber
  - fiber.start.md: 'Fiber::start »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::construct'
---
# Fiber::construct

(PHP 8> = 8.1.0)

Fiber::construct - Створює новий екземпляр Fiber

### Опис

public **Fiber::construct**[callable](language.types.callable.md) `$callback`

### Список параметрів

`callback`

[callable](language.types.callable.md)функція виклику під час запуску файбера. Аргументи для [Fiber::start()](fiber.start.md) будуть надається як аргументи для даного викликаного об'єкта.
