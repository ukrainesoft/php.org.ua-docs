Факторіал

-   [« gmpexport](function.gmp-export.html)
    
-   [gmpgcd »](function.gmp-gcd.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Факторіал
    

# gmpfact

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpfact - Факторіал

### Опис

```methodsynopsis
gmp_fact(GMP|int|string $num): GMP
```

Обчислює факторіал (`num!`) числа `num`

### Список параметрів

`num`

Число, факторіал якого обчислюється.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpfact()****

```php
<?php
$fact1 = gmp_fact(5); // 5 * 4 * 3 * 2 * 1
echo gmp_strval($fact1) . "\n";

$fact2 = gmp_fact(50); // 50 * 49 * 48, ... и т.д.
echo gmp_strval($fact2) . "\n";
?>
```

Результат виконання цього прикладу:

```
120
30414093201713378043612608166064768844377641568960512000000000000
```