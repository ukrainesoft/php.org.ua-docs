Обчислення квадратного кореня

-   [« gmp\_sign](function.gmp-sign.html)
    
-   [gmp\_sqrtrem »](function.gmp-sqrtrem.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Обчислення квадратного кореня
    

# gmpsqrt

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpsqrt — Обчислення квадратного кореня

### Опис

```methodsynopsis
gmp_sqrt(GMP|int|string $num): GMP
```

Обчислює квадратний корінь числа `num`

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Ціла частина кореня як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpsqrt()****

```php
<?php
$sqrt1 = gmp_sqrt("9");
$sqrt2 = gmp_sqrt("7");
$sqrt3 = gmp_sqrt("1524157875019052100");

echo gmp_strval($sqrt1) . "\n";
echo gmp_strval($sqrt2) . "\n";
echo gmp_strval($sqrt3) . "\n";
?>
```

Результат виконання цього прикладу:

```
3
2
1234567890
```