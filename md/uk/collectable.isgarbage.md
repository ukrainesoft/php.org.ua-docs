---
navigation:
  - class.collectable.md: « Collectable
  - class.pool.md: Pool »
  - index.md: PHP Manual
  - class.collectable.md: Collectable
title: 'Collectable::isGarbage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collectable::isGarbage

(PECL pthreads >= 2.0.8)

Collectable::isGarbage — Визначає, чи позначений об'єкт як сміття

### Опис

```methodsynopsis
public Collectable::isGarbage(): true
```

Можна викликати в [Pool::collect()](pool.collect.md) визначення, чи є об'єкт сміттям.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Тип значення, що повертається тепер **`true`**; раніше було bool. |

### Дивіться також

-   [Pool::collect()](pool.collect.md) \- Збирає посилання на виконані завдання
