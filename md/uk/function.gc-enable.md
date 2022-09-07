---
navigation:
  - function.gc-disable.md: « gcdisable
  - function.gc-enabled.md: гкenabled »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: гкenable
---
# гкenable

(PHP 5> = 5.3.0, PHP 7, PHP 8)

гкenable — Включає збирач циклічних посилань

### Опис

```methodsynopsis
gc_enable(): void
```

Включає збирач циклічних посилань, встановлюючи [zend.enableгк](info.configuration.md#ini.zend.enable-gc) в `1`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [Сборка мусора](features.gc.md)
