---
navigation:
  - function.memory-get-peak-usage.md: « memory\_get\_peak\_usage
  - function.memory-reset-peak-usage.md: memory\_reset\_peak\_usage »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: memory\_get\_usage
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# memory\_get\_usage

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

memory\_get\_usage — Повертає кількість пам'яті для PHP.

### Опис

```methodsynopsis
memory_get_usage(bool $real_usage = false): int
```

Повертає кількість пам'яті в байтах, яка була виділена PHP-скрипту на даний момент.

### Список параметрів

`real_usage`

При наданні цього параметра значення\*\*`true`\*\* повертається загальний обсяг пам'яті, яку система виділила процесу PHP, включаючи сторінки, що не використовуються. Якщо параметр не заданий або передано аргумент **`false`**, функція повідомить лише про кількість пам'яті, зайняту PHP-скриптом.

> **Зауваження** :
> 
> PHP не відстежує пам'ять, яка виділялася не `emalloc()`

### Значення, що повертаються

Повертає кількість пам'яті у байтах.

### Приклади

**Пример #1 Пример использования**memory\_get\_usage()\*\*\*\*

```php
<?php
// Это просто пример, цифры ниже будут
// отличаться в зависимости от вашей системы

echo memory_get_usage() . "\n"; // 36640

$a = str_repeat("Hello", 4242);

echo memory_get_usage() . "\n"; // 57960

unset($a);

echo memory_get_usage() . "\n"; // 36744

?>
```

### Дивіться також

-   [memory\_get\_peak\_usage()](function.memory-get-peak-usage.md) \- Повертає пікове значення об'єму пам'яті, виділеної PHP
-   [memory\_limit](ini.core.md#ini.memory-limit)
