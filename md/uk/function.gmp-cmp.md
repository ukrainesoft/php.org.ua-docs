Порівняння чисел

-   [« gmpclrbit](function.gmp-clrbit.html)
    
-   [gmpcom »](function.gmp-com.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Порівняння чисел
    

# gmpcmp

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpcmp — Порівняння чисел

### Опис

```methodsynopsis
gmp_cmp(GMP|int|string $num1, GMP|int|string $num2): int
```

Порівнює два числа.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає позитивне значення, якщо `a > b`нуль, якщо `a = b` та негативне значення, якщо `a < b`

### Приклади

**Приклад #1 Приклад використання **gmpcmp()****

```php
<?php
$cmp1 = gmp_cmp("1234", "1000"); // больше
$cmp2 = gmp_cmp("1000", "1234"); // меньше
$cmp3 = gmp_cmp("1234", "1234"); // равны

echo "$cmp1 $cmp2 $cmp3\n";
?>
```

Результат виконання цього прикладу:

```
1 -1 0
```