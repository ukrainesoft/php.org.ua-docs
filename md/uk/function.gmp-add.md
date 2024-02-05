---
navigation:
  - function.gmp-abs.md: « gmp\_abs
  - function.gmp-and.md: gmp\_and »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_add
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_add

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_add — Складання чисел

### Опис

```methodsynopsis
gmp_add(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Складає два числа.

### Список параметрів

`num1`

Перший доданок.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Другий доданок.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Сума аргументів як GMP числа.

### Приклади

**Приклад #1 Приклад використання** gmp\_add()\*\*\*\*

```php
<?php
$sum = gmp_add("123456789012345", "76543210987655");
echo gmp_strval($sum) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
200000000000000
```
