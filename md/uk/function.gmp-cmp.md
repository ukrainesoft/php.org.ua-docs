---
navigation:
  - function.gmp-clrbit.md: « gmp\_clrbit
  - function.gmp-com.md: gmp\_com »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_cmp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_cmp

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_cmp — Порівняння чисел

### Опис

```methodsynopsis
gmp_cmp(GMP|int|string $num1, GMP|int|string $num2): int
```

Порівнює два числа.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає позитивне значення, якщо `a > b`нуль, якщо `a = b` та негативне значення, якщо `a < b`

### Приклади

**Приклад #1 Приклад використання** gmp\_cmp()\*\*\*\*

```php
<?php
$cmp1 = gmp_cmp("1234", "1000"); // больше
$cmp2 = gmp_cmp("1000", "1234"); // меньше
$cmp3 = gmp_cmp("1234", "1234"); // равны

echo "$cmp1 $cmp2 $cmp3\n";
?>
```

Результат виконання наведеного прикладу:

```
1 -1 0
```
