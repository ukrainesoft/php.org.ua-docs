---
navigation:
  - imagickdraw.setstrokeantialias.md: '« ImagickDraw::setStrokeAntialias'
  - imagickdraw.setstrokedasharray.md: 'ImagickDraw::setStrokeDashArray »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeColor

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeColor — Встановлює колір для обведення контурів об'єкта.

### Опис

```methodsynopsis
public ImagickDraw::setStrokeColor(ImagickPixel $stroke_pixel): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює колір для обведення контурів об'єкта.

### Список параметрів

`stroke_pixel`

Колір обведення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setStrokeColor()\*\*\*\*

```php
<?php
function setStrokeColor($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(5);

    $draw->line(100, 100, 400, 145);
    $draw->rectangle(100, 200, 225, 350);

    $draw->setStrokeOpacity(0.1);
    $draw->line(100, 120, 400, 165);
    $draw->rectangle(275, 200, 400, 350);

    $image = new \Imagick();
    $image->newImage(500, 400, $backgroundColor);
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
