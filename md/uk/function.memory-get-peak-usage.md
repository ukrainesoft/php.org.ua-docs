---
navigation:
  - function.ini-set.html: « iniset
  - function.memory-get-usage.html: memorygetusage »
  - index.html: PHP Manual
  - ref.info.html: Опції PHP/інформаційні функції
title: memorygetpeakusage
---
# memorygetpeakusage

(PHP 5> = 5.2.0, PHP 7, PHP 8)

memorygetpeakusage — Повертає пікове значення об'єму пам'яті, виділене PHP

### Опис

```methodsynopsis
memory_get_peak_usage(bool $real_usage = false): int
```

Повертає максимальний обсяг пам'яті в байтах, виділений PHP-скрипту.

### Список параметрів

`real_usage`

Передача **`true`** як цей аргумент дозволяє отримати реальний обсяг пам'яті, виділений системою. Якщо аргумент не заданий чи дорівнює **`false`**, повертаються відомості лише про пам'ять, виділену функцією `emalloc()`

### Значення, що повертаються

Повертає максимальний обсяг пам'яті у байтах.

### Дивіться також

-   [memorygetusage()](function.memory-get-usage.html) - Повертає кількість пам'яті, виділену для PHP
-   [memorylimit](ini.core.html#ini.memory-limit)
