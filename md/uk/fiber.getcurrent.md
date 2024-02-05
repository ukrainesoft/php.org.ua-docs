---
navigation:
  - fiber.suspend.md: '« Fiber::suspend'
  - class.weakreference.md: WeakReference »
  - index.md: PHP Manual
  - class.fiber.md: Fiber
title: 'Fiber::getCurrent'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Fiber::getCurrent

(PHP 8 >= 8.1.0)

Fiber::getCurrent — Отримує поточний екземпляр Fiber

### Опис

```methodsynopsis
public static Fiber::getCurrent(): ?Fiber
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає екземпляр, що виконується в даний момент. [Fiber](class.fiber.md)или\*\*`null`\*\*якщо метод викликається ззовні файбера.
