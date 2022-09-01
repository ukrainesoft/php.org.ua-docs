---
navigation:
  - function.gmp-root.html: « gmproot
  - function.gmp-scan0.html: gmpscan0 »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmprootrem
---
# gmprootrem

(PHP 5> = 5.6.0, PHP 7, PHP 8)

gmprootrem - Витягти корінь ступеня N і повернути його цілу частину і залишок

### Опис

```methodsynopsis
gmp_rootrem(GMP|int|string $num, int $nth): array
```

Витягує корінь ступеня `nth` з `num`, Повертає його цілу частину і залишок (залишок обчислюється шляхом віднімання з початкового числа цілочисельного результату в nth).

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`nth`

Позитивна кількість ступеня кореня `num`

### Значення, що повертаються

Масив з двома елементами, перший з яких дорівнює цілісній компоненті результату, а другий залишку. Обидва елементи повертаються як GMP-чисел.
