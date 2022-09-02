---
navigation:
  - function.gmp-setbit.md: « gmpsetbit
  - function.gmp-sqrt.md: gmpsqrt »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmpsign
---
# gmpsign

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

gmpsign — Знак числа

### Опис

```methodsynopsis
gmp_sign(GMP|int|string $num): int
```

Перевіряє знак числа.

### Список параметрів

`num`

Об'єкт [GMP](class.gmp.md), або рядок, що містить число, яке можна перетворити на тип int.

### Значення, що повертаються

Повертає 1, якщо `num` позитивне; -1, якщо `num` негативне; і 0, якщо `num` одно нулю.

### Приклади

**Приклад #1 Приклад використання **gmpsign()****

```php
<?php
// положительное
echo gmp_sign("500") . "\n";

// отрицательное
echo gmp_sign("-500") . "\n";

// ноль
echo gmp_sign("0") . "\n";
?>
```

Результат виконання цього прикладу:

```
1
-1
0
```

### Дивіться також

-   [gmpabs()](function.gmp-abs.md) - Абсолютна величина
-   [abs()](function.abs.md) - Абсолютне значення (модуль числа)
