---
navigation:
  - function.extension-loaded.html: « extensionloaded
  - function.gc-disable.html: гкdisable »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: гкcollectcycles
---
# гкcollectcycles

(PHP 5> = 5.3.0, PHP 7, PHP 8)

гкcollectcycles — Примусовий запуск збирача сміття

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

-   [Сборка мусора](features.gc.md)
