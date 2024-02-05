---
navigation:
  - function.gmp-perfect-power.md: « gmp\_perfect\_power
  - function.gmp-popcount.md: gmp\_popcount »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_perfect\_square
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_perfect\_square

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_perfect\_square - Перевірка числа на точний квадрат

### Опис

```methodsynopsis
gmp_perfect_square(GMP|int|string $num): bool
```

Перевіряє, чи число точним квадратом, тобто. квадратом цілого числа.

### Список параметрів

`num`

Перевірене на точний квадрат число.

Об'єкт [GMP](class.gmp.md), ціле число (int) або числовий рядок (string).

### Значення, що повертаються

Повертає **`true`**, якщо `num` є квадратом цілого числа, інакше повертає **`false`**

### Приклади

**Пример #1 Пример использования**gmp\_perfect\_square()\*\*\*\*

```php
<?php
// 3 * 3, точный квадрат
var_dump(gmp_perfect_square("9"));

// не является точным квадратом
var_dump(gmp_perfect_square("7"));

// 1234567890 * 1234567890, точный квадрат
var_dump(gmp_perfect_square("1524157875019052100"));
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(false)
bool(true)
```

### Дивіться також

-   [gmp\_perfect\_power()](function.gmp-perfect-power.md) - Перевірити, чи є число "досконалим ступенем"
-   [gmp\_sqrt()](function.gmp-sqrt.md) \- Обчислення квадратного кореня
-   [gmp\_sqrtrem()](function.gmp-sqrtrem.md) \- Квадратний корінь із залишком
