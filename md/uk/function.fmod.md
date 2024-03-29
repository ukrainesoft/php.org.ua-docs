---
navigation:
  - function.floor.md: « floor
  - function.hexdec.md: hexdec »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: fmod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fmod

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

fmod — Повертає дрібний залишок від розподілу по модулю

### Опис

```methodsynopsis
fmod(float $num1, float $num2): float
```

Повертає у вигляді числа з плаваючою точкою дробовий залишок від поділу ділимого `num1` на дільник `num2`. Залишок (r) буде визначено так: num1 = i \* num2 + r, де i - ціле число. Якщо `num2` не дорівнює нулю, то у змінної r буде той самий знак, що і у числа `num1` і величину, меншу або рівну величині числа `num2`

### Список параметрів

`num1`

Подільне.

`num2`

Дільник.

### Значення, що повертаються

Повертає у вигляді числа з плаваючою точкою залишок поділу `num1` `num2`

### Приклади

**Приклад #1 Приклад використання функції** fmod()\*\*\*\*

```php
<?php

$x = 5.7;
$y = 1.3;
$r = fmod($x, $y);
// Значение переменной $r равно 0.5, потому что 4 * 1.3 + 0.5 = 5.7

?>
```

### Дивіться також

-   [](language.operators.arithmetic.md)— Поділ із плаваючою точкою
-   [`%`](language.operators.arithmetic.md)— Цілочисельний модуль
-   [intdiv()](function.intdiv.md)— Цілочисельний поділ
