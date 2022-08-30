Обчислення залишку від цілого розподілу

-   [« gmplegendre](function.gmp-legendre.html)
    
-   [gmpmul »](function.gmp-mul.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Обчислення залишку від цілого розподілу
    

# gmpmod

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpmod — Обчислення залишку від цілого розподілу

### Опис

```methodsynopsis
gmp_mod(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює залишок від поділу числа `num1` на `num2`. Результат завжди невід'ємний, знак числа `num2` ігнорується.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Дільник (модуль).

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpmod()****

```php
<?php
$mod = gmp_mod("8", "3");
echo gmp_strval($mod) . "\n";
?>
```

Результат виконання цього прикладу:

```
2
```