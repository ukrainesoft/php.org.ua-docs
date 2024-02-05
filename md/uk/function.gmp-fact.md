---
navigation:
  - function.gmp-export.md: « gmp\_export
  - function.gmp-gcd.md: gmp\_gcd »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_fact
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_fact

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_fact - Факторіал

### Опис

```methodsynopsis
gmp_fact(GMP|int|string $num): GMP
```

Обчислює факторіал (`num!`) числа`num`

### Список параметрів

`num`

Число, факторіал якого обчислюється.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Приклад #1 Приклад використання** gmp\_fact()\*\*\*\*

```php
<?php
$fact1 = gmp_fact(5); // 5 * 4 * 3 * 2 * 1
echo gmp_strval($fact1) . "\n";

$fact2 = gmp_fact(50); // 50 * 49 * 48, ... и т.д.
echo gmp_strval($fact2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
120
30414093201713378043612608166064768844377641568960512000000000000
```
