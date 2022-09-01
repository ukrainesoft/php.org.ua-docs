---
navigation:
  - function.srand.md: « srand
  - function.tanh.md: tanh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: tan
---
# tan

(PHP 4, PHP 5, PHP 7, PHP 8)

tan - Тангенс

### Опис

```methodsynopsis
tan(float $num): float
```

**tan()** повертає тангенс параметра `num`. Параметр `num` задається у радіанах.

### Список параметрів

`num`

Значення у радіанах

### Значення, що повертаються

Тангенс кута `num`

### Приклади

**Приклад #1 Приклад використання **tan()****

```php
<?php

echo tan(M_PI_4); // 1

?>
```

### Дивіться також

-   [atan()](function.atan.md) - Арктангенс
-   [atan2()](function.atan2.md) - Арктангенс двох змінних
-   [sin()](function.sin.md) - Сінус
-   [cos()](function.cos.md) - Косінус
-   [tanh()](function.tanh.md) - гіперболічний тангенс
-   [deg2rad()](function.deg2rad.md) - Перетворює значення із градусів на радіани
