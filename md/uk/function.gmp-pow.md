Зводить число до ступеня

-   [« gmppopcount](function.gmp-popcount.html)
    
-   [gmppowm »](function.gmp-powm.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Зводить число до ступеня
    

# gmppow

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmppow — Зводить число до ступеня

### Опис

```methodsynopsis
gmp_pow(GMP|int|string $num, int $exponent): GMP
```

Зводить число `num` у ступінь `exponent`

### Список параметрів

`num`

Підстава ступеня.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`exponent`

Позитивний показник ступеня числа `num`

### Значення, що повертаються

Нове (результуюче) GMP число. Результатом прикладу `0^0` буде 1.

### Приклади

**Приклад #1 Приклад використання **gmppow()****

```php
<?php
$pow1 = gmp_pow("2", 31);
echo gmp_strval($pow1) . "\n";
$pow2 = gmp_pow("0", 0);
echo gmp_strval($pow2) . "\n";
$pow3 = gmp_pow("2", -1); // Отрицательный показатель степени вызовет предупреждение
echo gmp_strval($pow3) . "\n";
?>
```

Результат виконання цього прикладу:

```
2147483648
1
```