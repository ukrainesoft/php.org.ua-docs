---
navigation:
  - function.gmp-sign.md: « gmp\_sign
  - function.gmp-sqrtrem.md: gmp\_sqrtrem »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_sqrt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_sqrt

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_sqrt — Обчислення квадратного кореня

### Опис

```methodsynopsis
gmp_sqrt(GMP|int|string $num): GMP
```

Обчислює квадратний корінь числа `num`

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Ціла частина кореня як GMP числа.

### Приклади

**Пример #1 Пример использования**gmp\_sqrt()\*\*\*\*

```php
<?php
$sqrt1 = gmp_sqrt("9");
$sqrt2 = gmp_sqrt("7");
$sqrt3 = gmp_sqrt("1524157875019052100");

echo gmp_strval($sqrt1) . "\n";
echo gmp_strval($sqrt2) . "\n";
echo gmp_strval($sqrt3) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3
2
1234567890
```
