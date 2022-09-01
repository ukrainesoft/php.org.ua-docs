---
navigation:
  - function.decoct.html: « decoct
  - function.exp.html: exp »
  - index.html: PHP Manual
  - ref.math.html: Математичні функції
title: deg2rad
---
# deg2rad

(PHP 4, PHP 5, PHP 7, PHP 8)

deg2rad — Перетворює значення градусів на радіани

### Опис

```methodsynopsis
deg2rad(float $num): float
```

Функція перетворює `num` із градусів у радіани.

### Список параметрів

`num`

Кутова величина у градусах

### Значення, що повертаються

Еквівалент `num` у радіанах

### Приклади

**Приклад #1 Приклад використання **deg2rad()****

```php
<?php

echo deg2rad(45); // 0.785398163397
var_dump(deg2rad(45) === M_PI_4); // bool(true)

?>
```

### Дивіться також

-   [rad2deg()](function.rad2deg.html) - Перетворює значення з радіанів на градуси
