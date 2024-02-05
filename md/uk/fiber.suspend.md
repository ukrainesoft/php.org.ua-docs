---
navigation:
  - fiber.isterminated.md: '« Fiber::isTerminated'
  - fiber.getcurrent.md: 'Fiber::getCurrent »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::suspend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Fiber::suspend

(PHP 8 >= 8.1.0)

Fiber::suspend — Зупиняє виконання поточного файбера

### Опис

```methodsynopsis
public static Fiber::suspend(mixed $value = null): mixed
```

Зупиняє виконання поточного файбера. Значення, надане цим методом, буде повернено з виклику [Fiber::start()](fiber.start.md) [Fiber::resume()](fiber.resume.md) або [Fiber::throw()](fiber.throw.md), що переключив виконання поточного файбера.

Коли виконання файбера відновлюється, метод повертає значення, надане в [Fiber::resume()](fiber.resume.md). Якщо виконання файбера відновлюється за допомогою Fiber::throw, виняток, переданий цьому методу, буде викинуто під час виклику методу.

Якщо цей метод викликається ззовні файбера, буде викинуто помилку [FiberError](class.fibererror.md)

### Список параметрів

`value`

Значення, що повертається під час виклику [Fiber::start()](fiber.start.md) [Fiber::resume()](fiber.resume.md) або [Fiber::throw()](fiber.throw.md), що перемикають виконання поточного файбера.

### Значення, що повертаються

Значение, предоставленное[Fiber::resume()](fiber.resume.md)
