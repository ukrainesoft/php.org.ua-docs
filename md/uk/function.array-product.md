---
navigation:
  - function.array-pop.md: « array\_pop
  - function.array-push.md: array\_push »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_product
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_product

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

array\_product — Обчислює добуток значень масиву

### Опис

```methodsynopsis
array_product(array $array): int|float
```

Функция**array\_product()** повертає добуток значень масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає твір у вигляді цілого чи числа з плаваючою точкою.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер видає помилку рівня **`E_WARNING`**, коли значення масиву (`array`) неможливо перетворити на ціле число (int) або число з плаваючою точкою (float). Раніше масиви (array) та об'єкти (object) ігнорувалися, тоді як інші значення приводилися до цілої кількості (int). Більше того, об'єкти, що визначають числове наведення (наприклад, об'єкти класу [GMP](class.gmp.md)), тепер наводяться, а чи не ігноруються. |

### Приклади

**Приклад #1 Приклад використання функції **array\_product()****

```php
<?php

$a = array(2, 4, 6, 8);
echo "product(a) = " . array_product($a) . "\n";
echo "product(array()) = " . array_product(array()) . "\n";

?>
```

Результат виконання наведеного прикладу:

```
product(a) = 384
product(array()) = 1
```
