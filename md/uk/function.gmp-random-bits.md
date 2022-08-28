Випадкове число

-   [« gmp\_prob\_prime](function.gmp-prob-prime.html)
    
-   [gmp\_random\_range »](function.gmp-random-range.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Випадкове число
    

# gmprandombits

(PHP 5> = 5.6.3, PHP 7, PHP 8)

gmprandombits — Випадкове число

### Опис

```methodsynopsis
gmp_random_bits(int $bits): GMP
```

Генерує випадкове число. Число буде в діапазоні від 0 до (2 `bits`

Параметр `bits` має бути більше 0, а максимальне значення обмежене лише доступною оперативною пам'яттю.

### Список параметрів

`bits`

Кількість бітів.

### Значення, що повертаються

Випадкове число GMP.

### Приклади

**Приклад #1 Приклад використання **gmprandombits()****

```php
<?php
$rand1 = gmp_random_bits(3); // случайное число от 0 до 7
$rand2 = gmp_random_bits(5); // случайное число от 0 до 31

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

Результат виконання цього прикладу:

```
3
15
```