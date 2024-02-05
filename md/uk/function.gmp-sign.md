---
navigation:
  - function.gmp-setbit.md: « gmp\_setbit
  - function.gmp-sqrt.md: gmp\_sqrt »
  - index.md: PHP Manual
  - ref.gmp.md: GMP Функції
title: gmp\_sign
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gmp\_sign

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

gmp\_sign — Знак числа

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

**Приклад #1 Приклад використання** gmp\_sign()\*\*\*\*

```php
<?php
// положительное
echo gmp_sign("500") . "\n";

// отрицательное
echo gmp_sign("-500") . "\n";

// ноль
echo gmp_sign("0") . "\n";
?>
```

Результат виконання наведеного прикладу:

```
1
-1
0
```

### Дивіться також

-   [gmp\_abs()](function.gmp-abs.md) \- Абсолютна величина
-   [abs()](function.abs.md) \- Повертає абсолютну величину (модуль числа)
