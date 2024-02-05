---
navigation:
  - function.pow.md: « pow
  - function.round.md: round »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: rad2deg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rad2deg

(PHP 4, PHP 5, PHP 7, PHP 8)

rad2deg — Перетворює значення з радіанів на градуси

### Опис

```methodsynopsis
rad2deg(float $num): float
```

Функція перетворює значення `num` з радіанів у градуси.

### Список параметрів

`num`

Значення у радіанах.

### Значення, що повертаються

Повертає еквівалент аргументу `num` у градусах.

### Приклади

**Приклад #1 Приклад использования функции**rad2deg()\*\*\*\*

```php
<?php

echo rad2deg(M_PI_4); // 45

?>
```

### Дивіться також

-   [deg2rad()](function.deg2rad.md) \- Перетворює значення із градусів на радіани
