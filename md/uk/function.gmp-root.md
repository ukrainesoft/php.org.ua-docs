---
navigation:
  - function.gmp-random.md: « gmprandom
  - function.gmp-rootrem.md: gmprootrem »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmproot
---
# gmproot

(PHP 5> = 5.6.0, PHP 7, PHP 8)

gmproot - Витягти корінь ступеня N і повернути його цілу частину

### Опис

```methodsynopsis
gmp_root(GMP|int|string $num, int $nth): GMP
```

Витягує корінь ступеня `nth` з `num` і повертає цілу частину результату.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`nth`

Позитивна кількість ступеня кореня `num`

### Значення, що повертаються

Цілочисленну частину результату вилучення кореня у вигляді GMP-числа.
