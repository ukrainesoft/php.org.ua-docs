- [«gmp_gcd](function.gmp-gcd.md)
- [gmp_hamdist »](function.gmp-hamdist.md)

- [PHP Manual](index.md)
- [GMP Функції](ref.gmp.md)
- Обчислення НОД та множників

#gmp_gcdext

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp_gcdext — Обчислення НОД та множників

### Опис

**gmp_gcdext**([GMP](class.gmp.md)\|int\|string `$num1`,
[GMP](class.gmp.md)\|int\|string `$num2`): array

Обчислює величини g, s і t, у виразі `a * s + b * t = g = gcd (a, b) `,
де gcd – найбільший спільний дільник. Повертає масив, значення
якого відповідають значенням величин g, s та t.

Ця функція може використовуватися для вирішення Диофантових рівнянь з
двома змінними. Це такі рівняння, які мають лише
цілі рішення і мають вигляд: `a*x + b*y = c`. За додатковою
інформацією звертайтеся на [» сторінку "Діофантове рівняння" в MathWorld](http://mathworld.wolfram.com/DiophantineEquation.md)

### Список параметрів

`num1`
Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок
(string).

`num2`
Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок
(string).

### Значення, що повертаються

Масив (Array) GMP чисел.

### Приклади

**Приклад #1 Рішення лінійного рівняння Діофанту**

`<?php// Рішення рівняння a*s + b*t = g// де a = 12, b = 21, g = gcd(12, 21) = 3$a =   (21);$g = gmp_gcd($a, $b);$r = gmp_gcdext($a, $b);$check_gcd = (gmp_strval($g) == gmp_strval($r['g'])) ;$eq_res = gmp_add(gmp_mul($a, $r['s']), gmp_mul($b, $r['t']));$check_res = (gmp_strval($g) == gmp_strval($eq_res ));if ($check_gcd && $check_res) {    $fmt = "Solution: %d*%d + %d*%d = %d
";    printf($fmt, gmp_strval($a), gmp_strval($r['s']), gmp_strval($b),   gmp_strval($r['t']), gmp_strval($r['g'] ));} else {   echo "Помилка під час рішення рівняння
";}// висновок: Рішення: 12*2 + 21*-1 = 3?> `
