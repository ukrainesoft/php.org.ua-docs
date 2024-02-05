---
navigation:
  - function.gc-disable.md: « gc\_disable
  - function.gc-enabled.md: gc\_enabled »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: gc\_enable
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gc\_enable

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

gc\_enable — Включає збирач циклічних посилань

### Опис

```methodsynopsis
gc_enable(): void
```

Включає збирач циклічних посилань, встановлюючи [zend.enable\_gc](info.configuration.md#ini.zend.enable-gc)в

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Складання сміття](features.gc.md)
