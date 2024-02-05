---
navigation:
  - function.gmp-invert.md: « gmp\_invert
  - function.gmp-kronecker.md: gmp\_kronecker »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_jacobi
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_jacobi

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_jacobi — Символ Якобі

### Опис

```methodsynopsis
gmp_jacobi(GMP|int|string $num1, GMP|int|string $num2): int
```

Обчислює [» Символ Якобі](http://primes.utm.edu/glossary/page.php?sort=JacobiSymbol)для чисел`num1`и`num2`. . `num2` має бути позитивним та непарним.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

Має бути позитивним і непарним.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_jacobi()\*\*\*\*

```php
<?php
echo gmp_jacobi("1", "3") . "\n";
echo gmp_jacobi("2", "3") . "\n";
?>
```

Результат виконання наведеного прикладу:

```
1
0
```

### Дивіться також

-   [gmp\_kronecker()](function.gmp-kronecker.md) \- Символ Кронекера - Якобі
-   [gmp\_legendre()](function.gmp-legendre.md) \- Символ Лежандра
