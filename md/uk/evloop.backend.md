---
navigation:
  - class.evloop.md: « EvLoop
  - evloop.check.md: 'EvLoop::check »'
  - index.md: PHP Manual
  - class.evloop.md: EvLoop
title: 'EvLoop::backend'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvLoop::backend

(PECL ev >= 0.2.0)

EvLoop::backend — Повертає ціле число, що описує бекенд, який використовується libev

### Опис

```methodsynopsis
public
   EvLoop::backend(): int
```

Те саме, що [Ev::backend()](ev.backend.md)але для екземпляра циклу.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, що описує бекенд, який використовується libev. Дивіться [Ev::backend()](ev.backend.md)

### Дивіться також

-   [Ev::backend()](ev.backend.md) \- Повертає ціле число, що описує бекенд, що використовується libev
