Перевірка числа на точний квадрат

-   [« gmpperfectpower](function.gmp-perfect-power.html)
    
-   [gmppopcount »](function.gmp-popcount.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
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

-   [gmpperfectpower()](function.gmp-perfect-power.html) - Перевірити, чи є число "досконалим ступенем"
-   [gmpsqrt()](function.gmp-sqrt.html) - Обчислення квадратного кореня
-   [gmpsqrtrem()](function.gmp-sqrtrem.html) - Квадратний корінь із залишком