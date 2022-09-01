---
navigation:
  - class.collectable.md: « Collectable
  - class.pool.md: Pool »
  - index.md: PHP Manual
  - class.collectable.md: Collectable
title: 'Collectable::isGarbage'
---
# Collectable::isGarbage

(PECL pthreads >= 2.0.8)

Collectable::isGarbage — Визначає, чи позначений об'єкт як сміття

### Опис

```methodsynopsis
public Collectable::isGarbage(): bool
```

Можна викликати в [Pool::collect()](pool.collect.md) визначення, чи є об'єкт сміттям.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### Дивіться також

-   [Pool::collect()](pool.collect.md) - Збирає посилання на виконані завдання
