---
navigation:
  - imagickdraw.setstrokelinejoin.md: '« ImagickDraw::setStrokeLineJoin'
  - imagickdraw.setstrokeopacity.md: 'ImagickDraw::setStrokeOpacity »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeMiterLimit'
---
# ImagickDraw::setStrokeMiterLimit

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeMiterLimit — Задає межу зрізу обведення

### Опис

```methodsynopsis
public ImagickDraw::setStrokeMiterLimit(int $miterlimit): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Задає межу зрізу. Коли два відрізки лінії зустрічаються під гострим кутом і для lineJoin задані кутові стики, зріз може виходити далеко за межі товщини лінії, що обводить контур. 'miterLimit' накладає обмеження на відношення довжини зрізу до 'lineWidth'.

### Список параметрів

`miterlimit`

Межа зрізу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setStrokeMiterLimit()****

```php
<?php
function setStrokeMiterLimit($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeOpacity(0.6);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(10);

    $yOffset = 100;

    $draw->setStrokeLineJoin(\Imagick::LINEJOIN_MITER);

    for ($y = 0; $y < 3; $y++) {

        $draw->setStrokeMiterLimit(40 * $y);

        $points = [
            ['x' => 22 * 3, 'y' => 15 * 4 + $y * $yOffset],
            ['x' => 20 * 3, 'y' => 20 * 4 + $y * $yOffset],
            ['x' => 70 * 5, 'y' => 45 * 4 + $y * $yOffset],
        ];

        $draw->polygon($points);
    }

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    $image->setImageType(\Imagick::IMGTYPE_PALETTE);
    $image->setImageCompressionQuality(100);
    $image->stripImage();

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
