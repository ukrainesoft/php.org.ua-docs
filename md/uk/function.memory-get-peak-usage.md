---
navigation:
  - function.ini-set.md: « ini\_set
  - function.memory-get-usage.md: memory\_get\_usage »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: memory\_get\_peak\_usage
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# memory\_get\_peak\_usage

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

memory\_get\_peak\_usage — Повертає пікове значення об'єму пам'яті, виділеного PHP

### Опис

```methodsynopsis
memory_get_peak_usage(bool $real_usage = false): int
```

Повертає максимальний обсяг пам'яті в байтах, виділений PHP-скрипту.

### Список параметрів

`real_usage`

Передача\*\*`true`\*\* як цей аргумент дозволяє отримати реальний обсяг пам'яті, виділений системою. Якщо аргумент не заданий чи дорівнює **`false`**, повертаються відомості лише про пам'ять, виділену функцією `emalloc()`

### Значення, що повертаються

Повертає максимальний обсяг пам'яті у байтах.

### Дивіться також

-   [memory\_get\_usage()](function.memory-get-usage.md) \- Повертає кількість пам'яті, виділеної для PHP
-   [memory\_reset\_peak\_usage()](function.memory-reset-peak-usage.md) \- Скидає пікове значення об'єму пам'яті, виділеної PHP
-   [memory\_limit](ini.core.md#ini.memory-limit)
