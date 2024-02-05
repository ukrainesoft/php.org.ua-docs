---
navigation:
  - function.gmp-mul.md: « gmp\_mul
  - function.gmp-nextprime.md: gmp\_nextprime »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_neg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_neg

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_neg - Зміна знака числа

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

**Приклад #1 Приклад використання** gmp\_neg()\*\*\*\*

```php
<?php
$neg1 = gmp_neg("1");
echo gmp_strval($neg1) . "\n";
$neg2 = gmp_neg("-1");
echo gmp_strval($neg2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
-1
1
```
