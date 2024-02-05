---
navigation:
  - function.gmp-add.md: « gmp\_add
  - function.gmp-binomial.md: gmp\_binomial »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_and
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_and

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_and - Побітове І

### Опис

```methodsynopsis
gmp_and(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Обчислює побітове І двох GMP чисел.

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Результат побитового`І` як GMP числа.

### Приклади

**Пример #1 Пример использования**gmp\_and()\*\*\*\*

```php
<?php
$and1 = gmp_and("0xfffffffff4", "0x4");
$and2 = gmp_and("0xfffffffff4", "0x8");
echo gmp_strval($and1) . "\n";
echo gmp_strval($and2) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
4
0
```
