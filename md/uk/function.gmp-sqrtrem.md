---
navigation:
  - function.gmp-sqrt.md: « gmpsqrt
  - function.gmp-strval.md: gmpstrval »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpsqrtrem
---
# gmpsqrtrem

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpsqrtrem - Квадратний корінь із залишком

### Опис

```methodsynopsis
gmp_sqrtrem(GMP|int|string $num): array
```

Обчислює квадратний корінь числа із залишком.

### Список параметрів

`num`

Число, з якого витягується корінь.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає масив, в якому перший елемент - ціла частина кореня з числа `num`, а другий - залишок (тобто різниця чисел `num` та квадрата першого елемента масиву).

### Приклади

**Приклад #1 Приклад використання **gmpsqrtrem()****

```php
<?php
list($sqrt1, $sqrt1rem) = gmp_sqrtrem("9");
list($sqrt2, $sqrt2rem) = gmp_sqrtrem("7");
list($sqrt3, $sqrt3rem) = gmp_sqrtrem("1048576");

echo gmp_strval($sqrt1) . ", " . gmp_strval($sqrt1rem) . "\n";
echo gmp_strval($sqrt2) . ", " . gmp_strval($sqrt2rem) . "\n";
echo gmp_strval($sqrt3) . ", " . gmp_strval($sqrt3rem) . "\n";
?>
```

Результат виконання цього прикладу:

```
3, 0
2, 3
1024, 0
```
