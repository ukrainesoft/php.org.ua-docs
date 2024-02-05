---
navigation:
  - imagickdraw.roundrectangle.md: '« ImagickDraw::roundRectangle'
  - imagickdraw.setclippath.md: 'ImagickDraw::setClipPath »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::scale'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::scale

(PECL imagick 2, PECL imagick 3)

ImagickDraw::scale — Регулює коефіцієнт масштабування

### Опис

```methodsynopsis
public ImagickDraw::scale(float $x, float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Регулює коефіцієнт масштабування для застосування у горизонтальному та вертикальному напрямках до поточного координатного простору.

### Список параметрів

`x`

Горизонтальний коефіцієнт масштабування.

`y`

Вертикальний коефіцієнт масштабування.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::scale()\*\*\*\*

```php
<?php
function scale($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(4);
    $draw->setFillColor($fillColor);
    $draw->rectangle(200, 200, 300, 300);
    $draw->setFillColor($fillModifiedColor);
    $draw->scale(1.4, 1.4);
    $draw->rectangle(200, 200, 300, 300);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
