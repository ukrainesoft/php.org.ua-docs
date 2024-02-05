---
navigation:
  - imagickdraw.skewx.md: '« ImagickDraw::skewX'
  - imagickdraw.translate.md: 'ImagickDraw::translate »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::skewY'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::skewY

(PECL imagick 2, PECL imagick 3)

ImagickDraw::skewY — Нахиляє поточну систему координат по вертикалі

### Опис

```methodsynopsis
public ImagickDraw::skewY(float $degrees): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Нахиляє систему координат по вертикалі.

### Список параметрів

`degrees`

Градус нахилу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::skewY()\*\*\*\*

```php
<?php
function skewY($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor,
               $startX, $startY, $endX, $endY, $skew) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(2);
    $draw->setFillColor($fillColor);
    $draw->rectangle($startX, $startY, $endX, $endY);
    $draw->setFillColor($fillModifiedColor);
    $draw->skewY($skew);
    $draw->rectangle($startX, $startY, $endX, $endY);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
