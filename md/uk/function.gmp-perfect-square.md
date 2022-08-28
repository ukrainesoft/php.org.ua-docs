Перевірка числа на точний квадрат

-   [« gmp\_perfect\_power](function.gmp-perfect-power.html)
    
-   [gmp\_popcount »](function.gmp-popcount.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Перевірка числа на точний квадрат
    

# gmpperfectsquare

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpperfectsquare - Перевірка числа на точний квадрат

### Опис

```methodsynopsis
gmp_perfect_square(GMP|int|string $num): bool
```

Перевіряє, чи число точним квадратом, тобто. квадратом цілого числа.

### Список параметрів

`num`

Перевірене на точний квадрат число.

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає **`true`**, якщо `num` є квадратом цілого числа, інакше повертає **`false`**

### Приклади

**Приклад #1 Приклад використання **gmpperfectsquare()****

```php
<?php
// 3 * 3, точный квадрат
var_dump(gmp_perfect_square("9"));

// не является точным квадратом
var_dump(gmp_perfect_square("7"));

// 1234567890 * 1234567890, точный квадрат
var_dump(gmp_perfect_square("1524157875019052100"));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
bool(true)
```

### Дивіться також

-   [gmp\_perfect\_power()](function.gmp-perfect-power.html) - Перевірити, чи є число "досконалим ступенем"
-   [gmp\_sqrt()](function.gmp-sqrt.html) - Обчислення квадратного кореня
-   [gmp\_sqrtrem()](function.gmp-sqrtrem.html) - Квадратний корінь із залишком