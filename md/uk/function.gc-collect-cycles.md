---
navigation:
  - function.extension-loaded.md: « extension\_loaded
  - function.gc-disable.md: gc\_disable »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: gc\_collect\_cycles
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gc\_collect\_cycles

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gc\_collect\_cycles — Примусовий запуск збирача сміття

### Опис

```methodsynopsis
gc_collect_cycles(): int
```

Очевидно запускає механізм пошуку циклічних посилань.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість знайдених посилань.

### Дивіться також

-   [Складання сміття](features.gc.md)
