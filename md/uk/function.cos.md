---
navigation:
  - function.ceil.md: « ceil
  - function.cosh.md: cosh »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: cos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cos

(PHP 4, PHP 5, PHP 7, PHP 8)

cos - Обчислює косинус

### Опис

```methodsynopsis
cos(float $num): float
```

Функция**cos()** повертає косинус числа `num`Параметр`num` задають у радіанах.

### Список параметрів

`num`

Кут у радіанах.

### Значення, що повертаються

Повертає косинус кута `num`

### Приклади

**Пример #1 Пример использования функции**cos()\*\*\*\*

```php
<?php

echo cos(M_PI); // -1

?>
```

### Дивіться також

-   [acos()](function.acos.md) \- обчислює арккосинус
-   [sin()](function.sin.md) \- обчислює синус
-   [tan()](function.tan.md) \- обчислює тангенс
-   [deg2rad()](function.deg2rad.md) \- Перетворює значення із градусів на радіани
