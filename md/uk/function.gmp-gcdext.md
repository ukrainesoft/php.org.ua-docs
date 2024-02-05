---
navigation:
  - function.gmp-gcd.md: « gmp\_gcd
  - function.gmp-hamdist.md: gmp\_hamdist »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_gcdext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_gcdext

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_gcdext — Обчислення НОД та множників

### Опис

```methodsynopsis
gmp_gcdext(GMP|int|string $num1, GMP|int|string $num2): array
```

Обчислює величини g, s і t, у виразі `a*s + b*t = g = gcd(a,b)`, де gcd – найбільший спільний дільник. Повертає масив, значення якого відповідають значенням величин g, s та t.

Ця функція може використовуватися для вирішення рівнянь Діофантових з двома змінними. Це такі рівняння, які мають лише цілочисельні рішення та мають вигляд: `a*x + b*y = c`. За додатковою інформацією звертайтесь на [» сторінку "Діофантове рівняння" в MathWorld](http://mathworld.wolfram.com/DiophantineEquation.md)

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Масив (Array) GMP чисел.

### Приклади

**Приклад #1 Рішення лінійного рівняння Діофанту**

```php
<?php
// Решение уравнения a*s + b*t = g
// где a = 12, b = 21, g = gcd(12, 21) = 3
$a = gmp_init(12);
$b = gmp_init(21);
$g = gmp_gcd($a, $b);
$r = gmp_gcdext($a, $b);

$check_gcd = (gmp_strval($g) == gmp_strval($r['g']));
$eq_res = gmp_add(gmp_mul($a, $r['s']), gmp_mul($b, $r['t']));
$check_res = (gmp_strval($g) == gmp_strval($eq_res));

if ($check_gcd && $check_res) {
    $fmt = "Solution: %d*%d + %d*%d = %d\n";
    printf($fmt, gmp_strval($a), gmp_strval($r['s']), gmp_strval($b),
    gmp_strval($r['t']), gmp_strval($r['g']));
} else {
    echo "Ошибка во время решения уравнения\n";
}

// вывод: Решение: 12*2 + 21*-1 = 3
?>
```
