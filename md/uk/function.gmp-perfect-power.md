Перевірити, чи є число "досконалим ступенем"

-   [« gmpор](function.gmp-or.html)
    
-   [gmpperfectsquare »](function.gmp-perfect-square.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Перевірити, чи є число "досконалим ступенем"
    

# gmpperfectpower

(PHP 7> = 7.3.0, PHP 8)

gmpperfectpower — Перевірити, чи є число "досконалим ступенем"

### Опис

```methodsynopsis
gmp_perfect_power(GMP|int|string $num): bool
```

Перевіряє, чи є `num` досконалим ступенем. Ціле число є досконалим ступенем, якщо його можна одержати зведенням меншого цілого числа в цілий ступінь.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає **`true`**, якщо `num` є досконалим ступенем. В іншому випадку повертає **`false`**

### Дивіться також

-   [gmpperfectsquare()](function.gmp-perfect-square.html) - Перевірка числа на точний квадрат