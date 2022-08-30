Побітове виключне АБО

-   [« gmptestbit](function.gmp-testbit.html)
    
-   [GMP »](class.gmp.md)
    
-   [PHP Manual](index.md)
    
-   [GMP Функції](ref.gmp.md)
    
-   Побітове виключне АБО
    

# gmpxor

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpxor - Побітове виключне АБО

### Опис

```methodsynopsis
gmp_xor(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює побітове що виключає АБО (XOR) двох GMP чисел.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)ю

### Приклади

**Приклад #1 Приклад використання **gmpxor()****

```php
<?php
$xor1 = gmp_init("1101101110011101", 2);
$xor2 = gmp_init("0110011001011001", 2);

$xor3 = gmp_xor($xor1, $xor2);

echo gmp_strval($xor3, 2) . "\n";
?>
```

Результат виконання цього прикладу:

```
1011110111000100
```