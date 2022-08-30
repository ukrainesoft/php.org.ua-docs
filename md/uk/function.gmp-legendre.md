Лежандра символ.

-   [« gmplcm](function.gmp-lcm.html)
    
-   [gmpmod »](function.gmp-mod.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Лежандра символ.
    

# gmplegendre

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmplegendre - Символ Лежандра

### Опис

```methodsynopsis
gmp_legendre(GMP|int|string $num1, GMP|int|string $num2): int
```

Обчислює [»  символ Лежандра](http://primes.utm.edu/glossary/page.php?sort=LegendreSymbol) чисел `num1` і `num2`. . `num2` має бути непарним та позитивним.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

Має бути позитивним і непарним.

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmplegendre()****

```php
<?php
echo gmp_legendre("1", "3") . "\n";
echo gmp_legendre("2", "3") . "\n";
?>
```

Результат виконання цього прикладу:

```
1
0
```

### Дивіться також

-   [gmpjacobi()](function.gmp-jacobi.html) - Символ Якобі
-   [gmpkronecker()](function.gmp-kronecker.html) - Символ Кронекера - Якобі