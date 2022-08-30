Символ Якобі

-   [« gmpinvert](function.gmp-invert.html)
    
-   [gmpkronecker »](function.gmp-kronecker.html)
    
-   [PHP Manual](index.md)
    
-   [GMP Функції](ref.gmp.md)
    
-   Символ Якобі
    

# gmpjacobi

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpjacobi — Символ Якобі

### Опис

```methodsynopsis
gmp_jacobi(GMP|int|string $num1, GMP|int|string $num2): int
```

Обчислює [» Символ Якоби](http://primes.utm.edu/glossary/page.php?sort=JacobiSymbol) для чисел `num1` і `num2`. . `num2` має бути позитивним та непарним.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

Має бути позитивним і непарним.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)ю

### Приклади

**Приклад #1 Приклад використання **gmpjacobi()****

```php
<?php
echo gmp_jacobi("1", "3") . "\n";
echo gmp_jacobi("2", "3") . "\n";
?>
```

Результат виконання цього прикладу:

```
1
0
```

### Дивіться також

-   [gmpkronecker()](function.gmp-kronecker.html) - Символ Кронекера - Якобі
-   [gmplegendre()](function.gmp-legendre.html) - Символ Лежандра