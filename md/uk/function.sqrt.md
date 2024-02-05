---
navigation:
  - function.sinh.md: « sinh
  - function.tan.md: tan »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: sqrt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqrt

(PHP 4, PHP 5, PHP 7, PHP 8)

sqrt — Витягує квадратний корінь

### Опис

```methodsynopsis
sqrt(float $num): float
```

Повертає квадратний корінь числа, переданого у параметр `num`

### Список параметрів

`num`

Аргумент для обчислення.

### Значення, що повертаються

Повертає квадратний корінь числа, заданого у параметрі `num`, або нечисло (`NAN`) для негативних чисел.

### Приклади

**Приклад #1 Приклад использования функции**sqrt()\*\*\*\*

```php
<?php

// Точность зависит от настроек директивы precision
echo sqrt(9); // 3
echo sqrt(10); // 3.16227766 ...

?>
```

### Дивіться також

-   [pow()](function.pow.md) \- Зводить у ступінь
-   **`M_SQRTPI`** `sqrt(pi)`
-   **`M_2_SQRTPI`** `2/sqrt(pi)`
-   **`M_SQRT2`** `sqrt(2)`
-   **`M_SQRT3`** `sqrt(3)`
-   **`M_SQRT1_2`** `1/sqrt(2)`
