Квадратний корінь

-   [« sinh](function.sinh.html)
    
-   [srand »](function.srand.html)
    
-   [PHP Manual](index.html)
    
-   [Математические функции](ref.math.html)
    
-   Квадратний корінь
    

# sqrt

(PHP 4, PHP 5, PHP 7, PHP 8)

sqrt - Квадратний корінь

### Опис

```methodsynopsis
sqrt(float $num): float
```

Повертає квадратний корінь з `num`

### Список параметрів

`num`

Аргумент для обчислення

### Значення, що повертаються

Квадратний корінь з `num` або спеціальне значення `NAN` для негативних чисел.

### Приклади

**Приклад #1 Приклад використання **sqrt()****

```php
<?php
// Точность зависит от ваших настроек точности
echo sqrt(9); // 3
echo sqrt(10); // 3.16227766 ...
?>
```

### Дивіться також

-   [pow()](function.pow.html) - Зведення в ступінь
-   **`M_SQRTPI`** `sqrt(pi)`
-   **`M_2_SQRTPI`** `2/sqrt(pi)`
-   **`M_SQRT2`** `sqrt(2)`
-   **`M_SQRT3`** `sqrt(3)`
-   **`M_SQRT1_2`** `1/sqrt(2)`