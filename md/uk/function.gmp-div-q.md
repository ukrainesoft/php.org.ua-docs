---
navigation:
  - function.gmp-com.md: « gmpcom
  - function.gmp-div-qr.md: gmpdivqr »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpdivдо
---
# gmpdivдо

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpdivq — Розподіл чисел

### Опис

```methodsynopsis
gmp_div_q(GMP|int|string $num1, GMP|int|string $num2, int $rounding_mode = GMP_ROUND_ZERO): GMP
```

ділить `num1` на `num2` і повертає цілий результат.

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`rounding_mode`

Округлення результату визначається параметром `rounding_mode`, який може приймати такі значення:

-   **`GMP_ROUND_ZERO`**: Дробова частина просто відрізається
-   **`GMP_ROUND_PLUSINF`**: Результат округляється до найближчого цілого убік `+бесконечности`
-   **`GMP_ROUND_MINUSINF`**: Результат округляється до найближчого цілого убік `-бесконечности`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)ю

### Приклади

**Приклад #1 Приклад використання **gmpdivq()****

```php
<?php
     $div1 = gmp_div_q("100", "5");
     echo gmp_strval($div1) . "\n";

     $div2 = gmp_div_q("1", "3");
     echo gmp_strval($div2) . "\n";

     $div3 = gmp_div_q("1", "3", GMP_ROUND_PLUSINF);
     echo gmp_strval($div3) . "\n";

     $div4 = gmp_div_q("-1", "4", GMP_ROUND_PLUSINF);
     echo gmp_strval($div4) . "\n";

     $div5 = gmp_div_q("-1", "4", GMP_ROUND_MINUSINF);
     echo gmp_strval($div5) . "\n";
     ?>
```

Результат виконання цього прикладу:

```
20
     0
     1
     0
     -1
```

### Примітки

> **Зауваження**
> 
> Ця функція має псевдонім [gmpdiv()](function.gmp-div.md)

### Дивіться також

-   [gmpdivr()](function.gmp-div-r.md) - Залишок від розподілу чисел
-   [gmpdivqr()](function.gmp-div-qr.md) - Поділ чисел та отримання приватного та залишку
