---
navigation:
  - function.round.md: « round
  - function.sinh.md: sinh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: sin
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sin

(PHP 4, PHP 5, PHP 7, PHP 8)

sin — Обчислює синус

### Опис

```methodsynopsis
sin(float $num): float
```

Функция**sin()** повертає синус числа `num`Параметр`num` задають у радіанах.

### Список параметрів

`num`

Значення у радіанах.

### Значення, що повертаються

Повертає синус кута `num`

### Приклади

**Приклад #1 Приклад використання функції** sin()\*\*\*\*

```php
<?php

// Точность зависит от настроек директивы precision
echo sin(deg2rad(60));  //  0.866025403 ...
echo sin(60);           // -0.304810621 ...

?>
```

### Дивіться також

-   [asin()](function.asin.md) \- обчислює арксинус
-   [sinh()](function.sinh.md) \- обчислює гіперболічний синус
-   [cos()](function.cos.md) \- обчислює косинус
-   [tan()](function.tan.md) \- обчислює тангенс
-   [deg2rad()](function.deg2rad.md) \- Перетворює значення із градусів на радіани
