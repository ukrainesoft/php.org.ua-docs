---
navigation:
  - function.gmp-mod.md: « gmp\_mod
  - function.gmp-neg.md: gmp\_neg »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_mul
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_mul

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_mul — Збільшення чисел

### Опис

```methodsynopsis
gmp_mul(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Помножує число `num1`на`num2` та повертає результат.

### Список параметрів

`num1`

Перший множник, число, що множиться на `num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Другий множник, число, що множиться на `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Приклад #1 Приклад використання** gmp\_mul()\*\*\*\*

```php
<?php
$mul = gmp_mul("12345678", "2000");
echo gmp_strval($mul) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
24691356000
```
