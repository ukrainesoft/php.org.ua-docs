---
navigation:
  - function.gmp-pow.md: « gmp\_pow
  - function.gmp-prob-prime.md: gmp\_prob\_prime »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_powm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_powm

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_powm - Зводить число в ступінь і робить розподіл за модулем

### Опис

```methodsynopsis
gmp_powm(GMP|int|string $num, GMP|int|string $exponent, GMP|int|string $modulus): GMP
```

Обчислює (`num`возводится в степень`exponent`) остаток от целочисленного деления на`modulus`. Якщо `exponent` від'ємний, результат не визначено.

### Список параметрів

`num`

Підстава ступеня.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`exponent`

Позитивний показник ступеня, в який зводиться `num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`modulus`

Дільник, залишок від цілого розподілу на який буде повернутий.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Нове число GMP (результат операції).

### Приклади

**Приклад #1 Приклад використання** gmp\_powm()\*\*\*\*

```php
<?php
$pow1 = gmp_powm("2", "31", "2147483649");
echo gmp_strval($pow1) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
2147483648
```
