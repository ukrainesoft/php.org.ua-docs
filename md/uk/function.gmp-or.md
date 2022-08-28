Побітове АБО

-   [« gmp\_nextprime](function.gmp-nextprime.html)
    
-   [gmp\_perfect\_power »](function.gmp-perfect-power.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Побітове АБО
    

# gmpор

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpor — Побітове АБО

### Опис

```methodsynopsis
gmp_or(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює побітове АБО двох GMP чисел.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpor()****

```php
<?php
$or1 = gmp_or("0xfffffff2", "4");
echo gmp_strval($or1, 16) . "\n";
$or2 = gmp_or("0xfffffff2", "2");
echo gmp_strval($or2, 16) . "\n";
?>
```

Результат виконання цього прикладу:

```
fffffff6
fffffff2
```