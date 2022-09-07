---
navigation:
  - function.gmp-div-q.md: « gmpdivдо
  - function.gmp-div-r.md: gmpdivr »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpdivгр
---
# gmpdivгр

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpdivqr — Поділ чисел та отримання приватного та залишку

### Опис

```methodsynopsis
gmp_div_qr(GMP|int|string $num1, GMP|int|string $num2, int $rounding_mode = GMP_ROUND_ZERO): array
```

Функція ділить `num1` на `num2`

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`rounding_mode`

У документації до функції [gmpdivq()](function.gmp-div-q.md) наведено опис аргументу `rounding_mode`

### Значення, що повертаються

Повертає масив (array), у якому перший елемент містить `[n/d]` (ціле приватне), а другий `(n - [n/d] * d)` (остача від ділення).

### Приклади

**Приклад #1 Поділ GMP чисел**

```php
<?php
     $a = gmp_init("0x41682179fbf5");
     $res = gmp_div_qr($a, "0xDEFE75");
     printf("Результат: q - %s, r - %s",
     gmp_strval($res[0]), gmp_strval($res[1]));
     ?>
```

### Дивіться також

-   [gmpdivq()](function.gmp-div-q.md) - Розподіл чисел
-   [gmpdivr()](function.gmp-div-r.md) - Залишок від розподілу чисел
