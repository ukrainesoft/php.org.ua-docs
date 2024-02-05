---
navigation:
  - function.gmp-kronecker.md: « gmp\_kronecker
  - function.gmp-legendre.md: gmp\_legendre »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_lcm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_lcm

(PHP 7 >= 7.3.0, PHP 8)

gmp\_lcm - Обчислює найменше загальне кратне

### Опис

```methodsynopsis
gmp_lcm(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Функція обчислює найменший загальний кратний для заданих `num1`и`num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Дивіться також

-   [gmp\_gcd()](function.gmp-gcd.md) \- Обчислення найбільшого спільного дільника
