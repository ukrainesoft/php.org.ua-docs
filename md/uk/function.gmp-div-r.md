---
navigation:
  - function.gmp-div-qr.md: « gmp\_div\_qr
  - function.gmp-div.md: gmp\_div »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_div\_r
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_div\_r

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_div\_r - Залишок від розподілу чисел

### Опис

```methodsynopsis
gmp_div_r(GMP|int|string $num1, GMP|int|string $num2, int $rounding_mode = GMP_ROUND_ZERO): GMP
```

Обчислює залишок від поділу націло числа `num1`на`num2`. Якщо число `num1` На відміну від нуля, результат буде мати знак цього числа.

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`rounding_mode`

В документации к функции[gmp\_div\_q()](function.gmp-div-q.md)приведено описание аргумента`rounding_mode`

### Значення, що повертаються

Залишок як GMP числа.

### Приклади

**Пример #1 Пример использования**gmp\_div\_r()\*\*\*\*

```php
<?php
     $div = gmp_div_r("105", "20");
     echo gmp_strval($div) . "\n";
     ?>
```

Результат виконання наведеного прикладу:

```
5
```

### Дивіться також

-   [gmp\_div\_q()](function.gmp-div-q.md) \- Розподіл чисел
-   [gmp\_div\_qr()](function.gmp-div-qr.md) \- Поділ чисел та отримання приватного та залишку
