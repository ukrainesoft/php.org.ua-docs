---
navigation:
  - function.gmp-root.md: « gmp\_root
  - function.gmp-scan0.md: gmp\_scan0 »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_rootrem
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_rootrem

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

gmp\_rootrem - Витягти корінь ступеня N і повернути його цілу частину і залишок

### Опис

```methodsynopsis
gmp_rootrem(GMP|int|string $num, int $nth): array
```

Извлекает корень степени`nth`из`num`, Повертає його цілу частину і залишок (залишок обчислюється шляхом віднімання з початкового числа цілого результату в ступені nth).

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`nth`

Позитивна кількість ступеня кореня `num`

### Значення, що повертаються

Масив з двома елементами, перший з яких дорівнює цілісній компоненті результату, а другий залишку. Обидва елементи повертаються як GMP-чисел.
