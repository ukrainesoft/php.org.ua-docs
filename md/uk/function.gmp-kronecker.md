---
navigation:
  - function.gmp-jacobi.md: « gmpjacobi
  - function.gmp-lcm.md: gmplcm »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpkronecker
---
# gmpkronecker

(PHP 7> = 7.3.0, PHP 8)

gmpkronecker - Символ Кронекера - Якобі

### Опис

```methodsynopsis
gmp_kronecker(GMP|int|string $num1, GMP|int|string $num2): int
```

Здійснює обчислення символу Кронекера - Якобі для `num1` і `num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає символ Кронекера - Якобі для `num1` і `num2`

### Дивіться також

-   [gmpjacobi()](function.gmp-jacobi.md) - Символ Якобі
-   [gmplegendre()](function.gmp-legendre.md) - Символ Лежандра
