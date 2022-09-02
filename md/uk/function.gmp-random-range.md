---
navigation:
  - function.gmp-random-bits.md: « gmprandombits
  - function.gmp-random-seed.md: gmprandomseed »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmprandomrange
---
# gmprandomrange

(PHP 5> = 5.6.3, PHP 7, PHP 8)

gmprandomrange - Випадкове число

### Опис

```methodsynopsis
gmp_random_range(GMP|int|string $min, GMP|int|string $max): GMP
```

Генерує випадкове число в діапазоні від `min` до `max`

`min` і `max` можуть бути негативними, але `min` у будь-якому випадку має бути менше `max`

### Список параметрів

`min`

GMP-число, яке є нижньою межею діапазону

`max`

GMP-число, що є верхньою межею діапазону

### Значення, що повертаються

Випадкове число GMP.

### Приклади

**Приклад #1 Приклад використання **gmprandomrange()****

```php
<?php
$rand1 = gmp_random_range(0, 100);    // случайное число от 0 до 100
$rand2 = gmp_random_range(-100, -10); // случайное число от -100 до -10

echo gmp_strval($rand1) . "\n";
echo gmp_strval($rand2) . "\n";
?>
```

Результат виконання цього прикладу:

```
42
-67
```
