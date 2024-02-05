---
navigation:
  - function.gmp-com.md: « gmp\_com
  - function.gmp-div-qr.md: gmp\_div\_qr »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_div\_q
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_div\_q

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_div\_q — Розподіл чисел

### Опис

```methodsynopsis
gmp_div_q(GMP|int|string $num1, GMP|int|string $num2, int $rounding_mode = GMP_ROUND_ZERO): GMP
```

ділить `num1`на`num2` і повертає цілий результат.

### Список параметрів

`num1`

Подільне.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Дільник числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`rounding_mode`

Округление результата определяется параметром`rounding_mode`, який може приймати такі значення:

-   **`GMP_ROUND_ZERO`**: Дробова частина просто відрізається
-   **`GMP_ROUND_PLUSINF`**: Результат округляється до найближчого цілого убік`+нескінченності`
-   **`GMP_ROUND_MINUSINF`**: Результат округляється до найближчого цілого убік`-нескінченності`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_div\_q()\*\*\*\*

```php
<?php
     $div1 = gmp_div_q("100", "5");
     echo gmp_strval($div1) . "\n";

     $div2 = gmp_div_q("1", "3");
     echo gmp_strval($div2) . "\n";

     $div3 = gmp_div_q("1", "3", GMP_ROUND_PLUSINF);
     echo gmp_strval($div3) . "\n";

     $div4 = gmp_div_q("-1", "4", GMP_ROUND_PLUSINF);
     echo gmp_strval($div4) . "\n";

     $div5 = gmp_div_q("-1", "4", GMP_ROUND_MINUSINF);
     echo gmp_strval($div5) . "\n";
     ?>
```

Результат виконання наведеного прикладу:

```
20
     0
     1
     0
     -1
```

### Примітки

> **Зауваження** :
> 
> Ця функція має псевдонім [gmp\_div()](function.gmp-div.md)

### Дивіться також

-   [gmp\_div\_r()](function.gmp-div-r.md) \- Залишок від розподілу чисел
-   [gmp\_div\_qr()](function.gmp-div-qr.md) \- Поділ чисел та отримання приватного та залишку
