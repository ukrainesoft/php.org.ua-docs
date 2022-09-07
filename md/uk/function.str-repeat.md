---
navigation:
  - function.str-pad.md: « strpad
  - function.str-replace.md: strreplace »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: strrepeat
---
# strrepeat

(PHP 4, PHP 5, PHP 7, PHP 8)

strrepeat — Повертає рядок, що повторюється.

### Опис

```methodsynopsis
str_repeat(string $string, int $times): string
```

Повертає рядок `string`, повторену `times` разів.

### Список параметрів

`string`

Повторюваний рядок.

`times`

Кількість разів, які потрібно повторити рядок `string`

`times` повинен бути більшим або дорівнює нулю. Якщо `times` дорівнює нулю, повертається порожній рядок.

### Значення, що повертаються

Повертає рядок, що повторюється.

### Приклади

**Приклад #1 Приклад використання **strrepeat()****

```php
<?php
echo str_repeat("-=", 10);
?>
```

Результат виконання цього прикладу:

```
-=-=-=-=-=-=-=-=-=-=
```

### Дивіться також

-   [for](control-structures.for.md)
-   [strpad()](function.str-pad.md) - Доповнює рядок іншим рядком до заданої довжини
-   [substrcount()](function.substr-count.md) - Повертає кількість входжень підрядка
