---
navigation:
  - function.gmp-div-qr.html: « gmpdivгр
  - function.gmp-div.html: gmpdiv »
  - index.html: PHP Manual
  - ref.gmp.html: GMP Функції
title: gmpdivр
---
# gmpdivр

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpdivr - Залишок від розподілу чисел

### Опис

```methodsynopsis
gmp_div_r(GMP|int|string $num1, GMP|int|string $num2, int $rounding_mode = GMP_ROUND_ZERO): GMP
```

Обчислює залишок від поділу націло числа `num1` на `num2`. Якщо число `num1` На відміну від нуля, результат буде мати знак цього числа.

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`rounding_mode`

У документації до функції [gmpdivq()](function.gmp-div-q.html) наведено опис аргументу `rounding_mode`

### Значення, що повертаються

Залишок як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpdivr()****

```php
<?php
     $div = gmp_div_r("105", "20");
     echo gmp_strval($div) . "\n";
     ?>
```

Результат виконання цього прикладу:

```
5
```

### Дивіться також

-   [gmpdivq()](function.gmp-div-q.html) - Розподіл чисел
-   [gmpdivqr()](function.gmp-div-qr.html) - Поділ чисел та отримання приватного та залишку
