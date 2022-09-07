---
navigation:
  - function.gmp-mul.md: « gmpmul
  - function.gmp-nextprime.md: gmpnextprime »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpneg
---
# gmpneg

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpneg - Зміна знака числа

### Опис

```methodsynopsis
gmp_neg(GMP|int|string $num): GMP
```

Повертає протилежне щодо нуля число.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає -`num` як GMP числа.

### Приклади

**Приклад #1 Приклад використання **gmpneg()****

```php
<?php
$neg1 = gmp_neg("1");
echo gmp_strval($neg1) . "\n";
$neg2 = gmp_neg("-1");
echo gmp_strval($neg2) . "\n";
?>
```

Результат виконання цього прикладу:

```
-1
1
```
