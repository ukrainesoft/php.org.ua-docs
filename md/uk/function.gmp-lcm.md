---
navigation:
  - function.gmp-kronecker.md: « gmpkronecker
  - function.gmp-legendre.md: gmplegendre »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmplcm
---
# gmplcm

(PHP 7> = 7.3.0, PHP 8)

gmplcm - Обчислює найменше загальне кратне

### Опис

```methodsynopsis
gmp_lcm(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Функція обчислює найменший загальний кратний для заданих `num1` і `num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)ю

### Дивіться також

-   [gmpgcd()](function.gmp-gcd.md) - Обчислення найбільшого спільного дільника
