---
navigation:
  - function.gmp-sqrt.md: « gmp\_sqrt
  - function.gmp-strval.md: gmp\_strval »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_sqrtrem
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_sqrtrem

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_sqrtrem - Квадратний корінь із залишком

### Опис

```methodsynopsis
gmp_sqrtrem(GMP|int|string $num): array
```

Обчислює квадратний корінь числа із залишком.

### Список параметрів

`num`

Число, з якого витягується корінь.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає масив, в якому перший елемент - ціла частина кореня з числа `num`, а другий - залишок (тобто різниця чисел `num` та квадрата першого елемента масиву).

### Приклади

**Пример #1 Пример использования**gmp\_sqrtrem()\*\*\*\*

```php
<?php
list($sqrt1, $sqrt1rem) = gmp_sqrtrem("9");
list($sqrt2, $sqrt2rem) = gmp_sqrtrem("7");
list($sqrt3, $sqrt3rem) = gmp_sqrtrem("1048576");

echo gmp_strval($sqrt1) . ", " . gmp_strval($sqrt1rem) . "\n";
echo gmp_strval($sqrt2) . ", " . gmp_strval($sqrt2rem) . "\n";
echo gmp_strval($sqrt3) . ", " . gmp_strval($sqrt3rem) . "\n";
?>
```

Результат виконання наведеного прикладу:

```
3, 0
2, 3
1024, 0
```
