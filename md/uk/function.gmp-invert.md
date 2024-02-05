---
navigation:
  - function.gmp-intval.md: « gmp\_intval
  - function.gmp-jacobi.md: gmp\_jacobi »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_invert
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_invert

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_invert — Інверсія залишку від розподілу

### Опис

```methodsynopsis
gmp_invert(GMP|int|string $num1, GMP|int|string $num2): GMP|false
```

Обчислює інверсію залишку від поділу числа `num1`на число`num2`

### Список параметрів

`num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

GMP число у разі успішного виконання або \*\*`false`\*\*якщо інверсія не існує.

### Приклади

**Пример #1 Пример использования**gmp\_invert()\*\*\*\*

```php
<?php
echo gmp_invert("5", "10"); // нет инверсии, не выводит ничего, результат FALSE
$invert = gmp_invert("5", "11");
echo gmp_strval($invert) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
9
```
