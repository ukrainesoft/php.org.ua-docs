Обчислення найбільшого спільного дільника

-   [« gmpfact](function.gmp-fact.html)
    
-   [gmpgcdext »](function.gmp-gcdext.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Обчислення найбільшого спільного дільника
    

# gmpgcd

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpgcd - Обчислення найбільшого спільного дільника

### Опис

```methodsynopsis
gmp_gcd(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює найбільший спільний дільник чисел `num1` і `num2`. Результат завжди позитивний, навіть якщо одне з чисел, або обидва негативні.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Позитивний НОД чисел `num1` і `num2`

### Приклади

**Приклад #1 Приклад використання **gmpgcd()****

```php
<?php
$gcd = gmp_gcd("12", "21");
echo gmp_strval($gcd) . "\n";
?>
```

Результат виконання цього прикладу:

```
3
```

### Дивіться також

-   [gmplcm()](function.gmp-lcm.html) - обчислює найменше загальне кратне