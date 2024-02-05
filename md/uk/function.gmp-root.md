---
navigation:
  - function.gmp-random.md: « gmp\_random
  - function.gmp-rootrem.md: gmp\_rootrem »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_root
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_root

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

gmp\_root - Витягти корінь ступеня N і повернути його цілу частину

### Опис

```methodsynopsis
gmp_root(GMP|int|string $num, int $nth): GMP
```

Извлекает корень степени`nth`из`num` і повертає цілу частину результату.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`nth`

Позитивна кількість ступеня кореня `num`

### Значення, що повертаються

Цілочисленну частину результату вилучення кореня у вигляді GMP-числа.
