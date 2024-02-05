---
navigation:
  - function.gc-collect-cycles.md: « gc\_collect\_cycles
  - function.gc-enable.md: gc\_enable »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: gc\_disable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gc\_disable

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gc\_disable — Вимикає збирач циклічних посилань

### Опис

```methodsynopsis
gc_disable(): void
```

Відключає збирач циклічних посилань шляхом встановлення значення [zend.enable\_gc](info.configuration.md#ini.zend.enable-gc)в

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Складання сміття](features.gc.md)
