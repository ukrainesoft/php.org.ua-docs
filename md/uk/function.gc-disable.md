---
navigation:
  - function.gc-collect-cycles.md: « gccollectcycles
  - function.gc-enable.md: гкenable »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: гкdisable
---
# гкdisable

(PHP 5> = 5.3.0, PHP 7, PHP 8)

гкdisable — Вимикає збирач циклічних посилань

### Опис

```methodsynopsis
gc_disable(): void
```

Відключає збирач циклічних посилань шляхом встановлення значення [zend.enableгк](info.configuration.md#ini.zend.enable-gc) в `0`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Сборка мусора](features.gc.md)
