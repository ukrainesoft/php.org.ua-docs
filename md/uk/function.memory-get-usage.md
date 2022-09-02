---
navigation:
  - function.memory-get-peak-usage.md: « memorygetpeakusage
  - function.php-ini-loaded-file.md: phpiniloadedfile »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: memorygetusage
---
# memorygetusage

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

memorygetusage — Повертає кількість пам'яті, виділену для PHP

### Опис

```methodsynopsis
memory_get_usage(bool $real_usage = false): int
```

Повертає кількість пам'яті в байтах, яка була виділена PHP-скрипту на даний момент.

### Список параметрів

`real_usage`

Передача **`true`** дозволяє дізнатися реальну кількість пам'яті, виділеної PHP скрипту системою, включаючи сторінки, що не використовуються. Якщо аргумент не заданий чи дорівнює **`false`**, буде повернуто лише кількість пам'яті, що використовується.

> **Зауваження**
> 
> PHP не відстежує пам'ять, яка виділялася не `emalloc()`

### Значення, що повертаються

Повертає кількість пам'яті у байтах.

### Приклади

**Приклад #1 Приклад використання **memorygetusage()****

```php
<?php
// Это просто пример, цифры ниже будут
// отличаться в зависимости от вашей системы

echo memory_get_usage() . "\n"; // 36640

$a = str_repeat("Hello", 4242);

echo memory_get_usage() . "\n"; // 57960

unset($a);

echo memory_get_usage() . "\n"; // 36744

?>
```

### Дивіться також

-   [memorygetpeakusage()](function.memory-get-peak-usage.md) - Повертає пікове значення об'єму пам'яті, виділене PHP
-   [memorylimit](ini.core.md#ini.memory-limit)
