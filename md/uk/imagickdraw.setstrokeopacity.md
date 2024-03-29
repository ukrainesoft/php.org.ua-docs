---
navigation:
  - imagickdraw.setstrokemiterlimit.md: '« ImagickDraw::setStrokeMiterLimit'
  - imagickdraw.setstrokepatternurl.md: 'ImagickDraw::setStrokePatternURL »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeOpacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeOpacity

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeOpacity — Визначає непрозорість обведення контурів об'єкта

### Опис

```methodsynopsis
public ImagickDraw::setStrokeOpacity(float $stroke_opacity): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Визначає непрозорість обведення контурів об'єкта.

### Список параметрів

`stroke_opacity`

Непрозорість обведення. 1.0 – повністю непрозора.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setStrokeOpacity()\*\*\*\*

```php
<?php
function setStrokeOpacity($strokeColor, $fillColor, $backgroundColor) {
    $draw = new \ImagickDraw();

    $draw->setStrokeWidth(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(10);
    $draw->setStrokeOpacity(1);
    $draw->line(100, 80, 400, 125);
    $draw->rectangle(25, 200, 150, 350);
    $draw->setStrokeOpacity(0.5);
    $draw->line(100, 100, 400, 145);
    $draw->rectangle(200, 200, 325, 350);
    $draw->setStrokeOpacity(0.2);
    $draw->line(100, 120, 400, 165);
    $draw->rectangle(375, 200, 500, 350);

    $image = new \Imagick();
    $image->newImage(550, 400, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
