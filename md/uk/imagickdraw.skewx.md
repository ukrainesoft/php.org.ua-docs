---
navigation:
  - imagickdraw.setviewbox.md: '« ImagickDraw::setViewbox'
  - imagickdraw.skewy.md: 'ImagickDraw::skewY »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::skewX'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::skewX

(PECL imagick 2, PECL imagick 3)

ImagickDraw::skewX — Нахиляє поточну систему координат по горизонталі.

### Опис

```methodsynopsis
public ImagickDraw::skewX(float $degrees): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Нахиляє систему координат по горизонталі.

### Список параметрів

`degrees`

Градус нахилу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::skewX()\*\*\*\*

```php
<?php
function skewX($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor,
               $startX, $startY, $endX, $endY, $skew) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(2);
    $draw->setFillColor($fillColor);
    $draw->rectangle($startX, $startY, $endX, $endY);
    $draw->setFillColor($fillModifiedColor);
    $draw->skewX($skew);
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
