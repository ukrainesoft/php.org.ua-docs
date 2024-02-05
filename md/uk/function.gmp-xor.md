---
navigation:
  - function.gmp-testbit.md: « gmp\_testbit
  - class.gmp.md: GMP »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_xor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_xor

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_xor - Побітове виключне АБО

### Опис

```methodsynopsis
gmp_xor(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює побітове що виключає АБО (XOR) двох GMP чисел.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_xor()\*\*\*\*

```php
<?php
$xor1 = gmp_init("1101101110011101", 2);
$xor2 = gmp_init("0110011001011001", 2);

$xor3 = gmp_xor($xor1, $xor2);

echo gmp_strval($xor3, 2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
1011110111000100
```
