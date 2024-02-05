---
navigation:
  - function.memory-get-usage.md: « memory\_get\_usage
  - function.php-ini-loaded-file.md: php\_ini\_loaded\_file »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: memory\_reset\_peak\_usage
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# memory\_reset\_peak\_usage

(PHP 8 >= 8.2.0)

memory\_reset\_peak\_usage — Скидає пікове значення об'єму пам'яті, виділеної PHP

### Опис

```methodsynopsis
memory_reset_peak_usage(): void
```

Скидає пікове значення об'єму виділеної пам'яті, яке повертається функцією [memory\_get\_peak\_usage()](function.memory-get-peak-usage.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** memory\_reset\_peak\_usage()\*\*\*\*

```php
<?php

var_dump(memory_get_peak_usage());

$a = str_repeat("Hello", 424242);
var_dump(memory_get_peak_usage());

unset($a);
memory_reset_peak_usage();

$a = str_repeat("Hello", 2424);
var_dump(memory_get_peak_usage());

?>
```

Висновок наведеного прикладу буде схожим на:

```
int(422440)
int(2508672)
int(399208)
```

### Дивіться також

-   [memory\_get\_peak\_usage()](function.memory-get-peak-usage.md) \- Повертає пікове значення об'єму пам'яті, виділеної PHP
