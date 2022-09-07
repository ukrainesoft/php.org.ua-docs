---
navigation:
  - function.gmp-add.md: « gmpadd
  - function.gmp-binomial.md: gmpbinomial »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpand
---
# gmpand

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpand - Побітове І

### Опис

```methodsynopsis
gmp_and(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює побітове І двох GMP чисел.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Результат побитового `И` як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpand()****

```php
<?php
$and1 = gmp_and("0xfffffffff4", "0x4");
$and2 = gmp_and("0xfffffffff4", "0x8");
echo gmp_strval($and1) . "\n";
echo gmp_strval($and2) . "\n";
?>
```

Результат виконання цього прикладу:

```
4
0
```
