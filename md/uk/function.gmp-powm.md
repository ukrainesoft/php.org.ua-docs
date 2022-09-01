---
navigation:
  - function.gmp-pow.html: « gmppow
  - function.gmp-prob-prime.html: gmpprobprime »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmppowm
---
# gmppowm

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmppowm - Зводить число в ступінь і робить розподіл за модулем

### Опис

```methodsynopsis
gmp_powm(GMP|int|string $num, GMP|int|string $exponent, GMP|int|string $modulus): GMP
```

Обчислює (`num` зводиться у ступінь `exponent`) залишок від цілісного поділу на `modulus`. Якщо `exponent` від'ємний, результат не визначено.

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

**Приклад #1 Приклад використання **gmppowm()****

```php
<?php
$pow1 = gmp_powm("2", "31", "2147483649");
echo gmp_strval($pow1) . "\n";
?>
```

Результат виконання цього прикладу:

```
2147483648
```
