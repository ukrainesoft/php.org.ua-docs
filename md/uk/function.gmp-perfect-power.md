---
navigation:
  - function.gmp-or.md: « gmp\_or
  - function.gmp-perfect-square.md: gmp\_perfect\_square »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_perfect\_power
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_perfect\_power

(PHP 7 >= 7.3.0, PHP 8)

gmp\_perfect\_power — Перевірити, чи є число "досконалим ступенем"

### Опис

```methodsynopsis
gmp_perfect_power(GMP|int|string $num): bool
```

Перевіряє, чи є `num` досконалим ступенем. Ціле число є досконалим ступенем, якщо його можна одержати зведенням меншого цілого числа в цілий ступінь.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає **`true`**, якщо `num` є досконалим ступенем. В іншому випадку повертає **`false`**

### Дивіться також

-   [gmp\_perfect\_square()](function.gmp-perfect-square.md) \- Перевірка числа на точний квадрат
