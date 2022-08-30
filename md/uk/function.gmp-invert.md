Інверсія залишку від розподілу

-   [« gmpintval](function.gmp-intval.html)
    
-   [gmpjacobi »](function.gmp-jacobi.html)
    
-   [PHP Manual](index.md)
    
-   [GMP Функції](ref.gmp.md)
    
-   Інверсія залишку від розподілу
    

# gmpinvert

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpinvert — Інверсія залишку від розподілу

### Опис

```methodsynopsis
gmp_invert(GMP|int|string $num1, GMP|int|string $num2): GMP|false
```

Обчислює інверсію залишку від поділу числа `num1` на число `num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

GMP число у разі успішного виконання або \*\*`false`\*\*якщо інверсія не існує.

### Приклади

**Приклад #1 Приклад використання **gmpinvert()****

```php
<?php
echo gmp_invert("5", "10"); // нет инверсии, не выводит ничего, результат FALSE
$invert = gmp_invert("5", "11");
echo gmp_strval($invert) . "\n";
?>
```

Результат виконання цього прикладу:

```
9
```