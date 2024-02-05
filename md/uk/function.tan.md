---
navigation:
  - function.sqrt.md: « sqrt
  - function.tanh.md: tanh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: tan
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# tan

(PHP 4, PHP 5, PHP 7, PHP 8)

tan - Обчислює тангенс

### Опис

```methodsynopsis
tan(float $num): float
```

Функция**tan()** повертає тангенс числа `num`Параметр`num` задають у радіанах.

### Список параметрів

`num`

Значення у радіанах.

### Значення, що повертаються

Возвращает тангенс угла`num`

### Приклади

**Приклад #1 Приклад использования функции**tan()\*\*\*\*

```php
<?php

echo tan(M_PI_4); // 1

?>
```

### Дивіться також

-   [atan()](function.atan.md) \- обчислює арктангенс
-   [atan2()](function.atan2.md) \- обчислює арктангенс двох змінних
-   [sin()](function.sin.md) \- обчислює синус
-   [cos()](function.cos.md) \- обчислює косинус
-   [tanh()](function.tanh.md) \- обчислює гіперболічний тангенс
-   [deg2rad()](function.deg2rad.md) \- Перетворює значення із градусів на радіани
