Кількість одиниць у двійковому записі числа

-   [« gmpperfectsquare](function.gmp-perfect-square.html)
    
-   [gmppow »](function.gmp-pow.html)
    
-   [PHP Manual](index.md)
    
-   [GMP Функції](ref.gmp.md)
    
-   Кількість одиниць у двійковому записі числа
    

# gmppopcount

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmppopcount — Кількість одиниць у двійковому записі числа

### Опис

```methodsynopsis
gmp_popcount(GMP|int|string $num): int
```

Повертає кількість одиниць у двійковому записі числа.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Кількість одиниць у двійковому записі числа `num`, як числа (int).

### Приклади

**Приклад #1 Приклад використання **gmppopcount()****

```php
<?php
$pop1 = gmp_init("10000101", 2); // 3 1's
echo gmp_popcount($pop1) . "\n";
$pop2 = gmp_init("11111110", 2); // 7 1's
echo gmp_popcount($pop2) . "\n";
?>
```

Результат виконання цього прикладу:

```
3
7
```