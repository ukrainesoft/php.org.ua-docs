---
navigation:
  - fiber.construct.md: '« Fiber::\_\_construct'
  - fiber.resume.md: 'Fiber::resume »'
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::start'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Fiber::start

(PHP 8 >= 8.1.0)

Fiber::start — Починає виконання файбера

### Опис

```methodsynopsis
public Fiber::start(mixed ...$args): mixed
```

Змінний список аргументів, що передається об'єкту, що викликається, використовується при побудові файбера.

Якщо під час виклику методу файбер вже було запущено, буде викинуто [FiberError](class.fibererror.md)

### Список параметрів

`args`

Аргументи, які слід використовувати при виклику об'єкта, що викликається, що передається конструктору файбера.

### Значення, що повертаються

Значення, надане під час першого виклику [Fiber::suspend()](fiber.suspend.md)или\*\*`null`\*\* у разі повернення файбера. Якщо файбер викинув виняток перед призупиненням, його буде викинуто з цього методу.
