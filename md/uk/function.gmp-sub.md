---
navigation:
  - function.gmp-strval.md: « gmp\_strval
  - function.gmp-testbit.md: gmp\_testbit »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_sub
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_sub

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_sub — Віднімання чисел

### Опис

```methodsynopsis
gmp_sub(GMP|int|string $num1, GMP|int|string $num2): GMP
```

Віднімає число `num2` з числа `num1` та повертає результат.

### Список параметрів

`num1`

Зменшуване.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

`num2`

Віднімається з числа `num1`

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Об'єкт класу [GMP](class.gmp.md)

### Приклади

**Пример #1 Пример использования**gmp\_sub()\*\*\*\*

```php
<?php
$sub = gmp_sub("281474976710656", "4294967296"); // 2^48 - 2^32
echo gmp_strval($sub) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
281470681743360
```
