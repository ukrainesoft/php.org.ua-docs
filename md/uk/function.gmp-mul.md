Розмноження чисел

-   [« gmp\_mod](function.gmp-mod.html)
    
-   [gmp\_neg »](function.gmp-neg.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Розмноження чисел
    

# gmpmul

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpmul — Збільшення чисел

### Опис

```methodsynopsis
gmp_mul(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Помножує число `num1` на `num2` та повертає результат.

### Список параметрів

`num1`

Перший множник, число, що множиться на `num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Другий множник, число, що множиться на `num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpmul()****

```php
<?php
$mul = gmp_mul("12345678", "2000");
echo gmp_strval($mul) . "\n";
?>
```

Результат виконання цього прикладу:

```
24691356000
```