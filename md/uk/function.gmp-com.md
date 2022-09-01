---
navigation:
  - function.gmp-cmp.html: « gmpcmp
  - function.gmp-div-q.html: gmpdivq »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpcom
---
# gmpcom

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpcom — Обчислює доповнення до одиниці числа

### Опис

```methodsynopsis
gmp_com(GMP|int|string $num): GMP
```

Повертає доповнення до одиниці числа `num`

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає доповнення до одиниці числа `num` як числа GMP.

### Приклади

**Приклад #1 Приклад використання **gmpcom()****

```php
<?php
$com = gmp_com("1234");
echo gmp_strval($com) . "\n";
?>
```

Результат виконання цього прикладу:

```
-1235
```
