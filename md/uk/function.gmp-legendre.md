---
navigation:
  - function.gmp-lcm.md: « gmp\_lcm
  - function.gmp-mod.md: gmp\_mod »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_legendre
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_legendre

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_legendre - Символ Лежандра

### Опис

```methodsynopsis
gmp_legendre(GMP|int|string $num1, GMP|int|string $num2): int
```

Обчислює [»  символ Лежандра](http://primes.utm.edu/glossary/page.php?sort=LegendreSymbol)чисел`num1`и`num2`. . `num2` має бути непарним та позитивним.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

Має бути позитивним і непарним.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_legendre()\*\*\*\*

```php
<?php
echo gmp_legendre("1", "3") . "\n";
echo gmp_legendre("2", "3") . "\n";
?>
```

Результат виконання наведеного прикладу:

```
1
0
```

### Дивіться також

-   [gmp\_jacobi()](function.gmp-jacobi.md) \- Символ Якобі
-   [gmp\_kronecker()](function.gmp-kronecker.md) \- Символ Кронекера - Якобі
