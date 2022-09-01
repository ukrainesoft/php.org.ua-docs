---
navigation:
  - imagickdraw.setviewbox.html: '« ImagickDraw::setViewbox'
  - imagickdraw.skewy.html: 'ImagickDraw::skewY »'
  - index.html: PHP Manual
  - class.imagickdraw.html: ImagickDraw
title: 'ImagickDraw::skewX'
---
# ImagickDraw::skewX

(PECL imagick 2, PECL imagick 3)

ImagickDraw::skewX — Нахиляє поточну систему координат по горизонталі.

### Опис

```methodsynopsis
public ImagickDraw::skewX(float $degrees): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Нахиляє систему координат по горизонталі.

### Список параметрів

`degrees`

Градус нахилу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::skewX()****

```php
<?php
function skewX($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor,
               $startX, $startY, $endX, $endY, $skew) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(2);
    $draw->setFillColor($fillColor);
    $draw->rectangle($startX, $startY, $endX, $endY);
    $draw->setFillColor($fillModifiedColor);
    $draw->skewX($skew);
    $draw->rectangle($startX, $startY, $endX, $endY);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
