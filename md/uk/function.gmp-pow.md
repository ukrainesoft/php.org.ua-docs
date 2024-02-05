---
navigation:
  - function.gmp-popcount.md: « gmp\_popcount
  - function.gmp-powm.md: gmp\_powm »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_pow
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_pow

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_pow — Зводить число до ступеня

### Опис

```methodsynopsis
gmp_pow(GMP|int|string $num, int $exponent): GMP
```

Зводить число `num`в степень`exponent`

### Список параметрів

`num`

Підстава ступеня.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`exponent`

Позитивний показник ступеня числа `num`

### Значення, що повертаються

Новое (результирующее) GMP число. Результатом Приклада`0^0`будет 1.

### Приклади

**Приклад #1 Приклад використання** gmp\_pow()\*\*\*\*

```php
<?php
$pow1 = gmp_pow("2", 31);
echo gmp_strval($pow1) . "\n";
$pow2 = gmp_pow("0", 0);
echo gmp_strval($pow2) . "\n";
$pow3 = gmp_pow("2", -1); // Отрицательный показатель степени вызовет предупреждение
echo gmp_strval($pow3) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2147483648
1
```
