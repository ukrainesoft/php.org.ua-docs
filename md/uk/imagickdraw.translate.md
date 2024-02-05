---
navigation:
  - imagickdraw.skewy.md: '« ImagickDraw::skewY'
  - class.imagickpixel.md: ImagickPixel »
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::translate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::translate

(PECL imagick 2, PECL imagick 3)

ImagickDraw::translate — Застосовує перенесення до поточної системи координат

### Опис

```methodsynopsis
public ImagickDraw::translate(float $x, float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Застосовує перенесення до поточної системи координат, яка переміщає початок системи координат у зазначену координату.

### Список параметрів

`x`

Горизонтальне перенесення.

`y`

Вертикальне перенесення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::translate()\*\*\*\*

```php
<?php
function translate($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor,
                   $startX, $startY, $endX, $endY, $translateX, $translateY) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->rectangle($startX, $startY, $endX, $endY);

    $draw->setFillColor($fillModifiedColor);
    $draw->translate($translateX, $translateY);
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
