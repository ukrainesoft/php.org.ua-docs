---
navigation:
  - function.gmp-jacobi.md: « gmp\_jacobi
  - function.gmp-lcm.md: gmp\_lcm »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_kronecker
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_kronecker

(PHP 7 >= 7.3.0, PHP 8)

gmp\_kronecker - Символ Кронекера - Якобі

### Опис

```methodsynopsis
gmp_kronecker(GMP|int|string $num1, GMP|int|string $num2): int
```

Здійснює обчислення символу Кронекера - Якобі для `num1`и`num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає символ Кронекера - Якобі для `num1`и`num2`

### Дивіться також

-   [gmp\_jacobi()](function.gmp-jacobi.md) \- Символ Якобі
-   [gmp\_legendre()](function.gmp-legendre.md) \- Символ Лежандра
