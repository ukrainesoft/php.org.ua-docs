---
navigation:
  - function.gmp-perfect-square.md: « gmp\_perfect\_square
  - function.gmp-pow.md: gmp\_pow »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_popcount
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_popcount

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_popcount — Кількість одиниць у двійковому записі числа

### Опис

```methodsynopsis
gmp_popcount(GMP|int|string $num): int
```

Повертає кількість одиниць у двійковому записі числа.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Кількість одиниць у двійковому записі числа `num`, як числа (int).

### Приклади

**Приклад #1 Приклад використання** gmp\_popcount()\*\*\*\*

```php
<?php
$pop1 = gmp_init("10000101", 2); // 3 1's
echo gmp_popcount($pop1) . "\n";
$pop2 = gmp_init("11111110", 2); // 7 1's
echo gmp_popcount($pop2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
7
```
