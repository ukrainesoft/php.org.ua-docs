Віднімання чисел

-   [« gmp\_strval](function.gmp-strval.html)
    
-   [gmp\_testbit »](function.gmp-testbit.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Віднімання чисел
    

# gmpsub

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpsub — Віднімання чисел

### Опис

```methodsynopsis
gmp_sub(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Віднімає число `num2` з числа `num1` та повертає результат.

### Список параметрів

`num1`

Зменшуване.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

`num2`

Віднімається з числа `num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.html)ю

### Приклади

**Приклад #1 Приклад використання **gmpsub()****

```php
<?php
$sub = gmp_sub("281474976710656", "4294967296"); // 2^48 - 2^32
echo gmp_strval($sub) . "\n";
?>
```

Результат виконання цього прикладу:

```
281470681743360
```