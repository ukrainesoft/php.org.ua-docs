---
navigation:
  - function.round.md: « round
  - function.sinh.md: sinh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: sin
---
# sin

(PHP 4, PHP 5, PHP 7, PHP 8)

sin - Сінус

### Опис

```methodsynopsis
sin(float $num): float
```

**sin()** повертає синус параметра `num`. Параметр `num` задається у радіанах.

### Список параметрів

`num`

Значення у радіанах

### Значення, що повертаються

Синус кута `num`

### Приклади

**Приклад #1 Приклад використання **sin()****

```php
<?php

// Точность зависит от ваших настроек точности
echo sin(deg2rad(60));  //  0.866025403 ...
echo sin(60);           // -0.304810621 ...

?>
```

### Дивіться також

-   [asin()](function.asin.md) - Арксінус
-   [sinh()](function.sinh.md) - Гіперболічний синус
-   [cos()](function.cos.md) - Косінус
-   [tan()](function.tan.md) - Тангенс
-   [deg2rad()](function.deg2rad.md) - Перетворює значення із градусів на радіани
