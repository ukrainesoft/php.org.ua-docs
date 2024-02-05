---
navigation:
  - function.decoct.md: « decoct
  - function.exp.md: exp »
  - index.md: PHP Manual
  - ref.math.md: Математичні функції
title: deg2rad
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# deg2rad

(PHP 4, PHP 5, PHP 7, PHP 8)

deg2rad — Перетворює значення градусів на радіани

### Опис

```methodsynopsis
deg2rad(float $num): float
```

Функція перетворює значення параметра `num` із градусів у радіани.

### Список параметрів

`num`

Кутова величина у градусах.

### Значення, що повертаються

Повертає еквівалент аргументу `num` у радіанах.

### Приклади

**Пример #1 Пример использования функции**deg2rad()\*\*\*\*

```php
<?php

echo deg2rad(45); // 0.785398163397
var_dump(deg2rad(45) === M_PI_4); // bool(true)

?>
```

### Дивіться також

-   [rad2deg()](function.rad2deg.md) \- Перетворює значення з радіанів на градуси
