Відстань Хеммінга

-   [« gmp\_gcdext](function.gmp-gcdext.html)
    
-   [gmp\_import »](function.gmp-import.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Відстань Хеммінга
    

# gmphamdist

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmphamdist — Відстань Хеммінга

### Опис

```methodsynopsis
gmp_hamdist(GMP|int|string $num1, GMP|int|string $num2): int
```

Повертає відстань Хеммінгу для чисел `num1` і `num2`. Обидва операнда мають бути невід'ємними.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

Має бути невід'ємним.

`num2`

Об'єкт [GMP](class.gmp.html), ціле число (int) або числовий рядок (string).

Має бути невід'ємним.

### Значення, що повертаються

Відстань Хеммінга між `num1` і `num2` як цілого числа (int).

### Приклади

**Приклад #1 Приклад використання **gmphamdist()****

```php
<?php
$ham1 = gmp_init("1001010011", 2);
$ham2 = gmp_init("1011111100", 2);
echo gmp_hamdist($ham1, $ham2) . "\n";

/* расстояние Хэмминга эквивалентно: */
echo gmp_popcount(gmp_xor($ham1, $ham2)) . "\n";
?>
```

Результат виконання цього прикладу:

```
6
6
```

### Дивіться також

-   [gmp\_popcount()](function.gmp-popcount.html) - Кількість одиниць у двійковому записі числа
-   [gmp\_xor()](function.gmp-xor.html) - Побітове що виключає АБО