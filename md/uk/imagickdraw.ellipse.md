---
navigation:
  - imagickdraw.destroy.md: '« ImagickDraw::destroy'
  - imagickdraw.getclippath.md: 'ImagickDraw::getClipPath »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::ellipse'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::ellipse

(PECL imagick 2, PECL imagick 3)

ImagickDraw::ellipse — Малює на зображенні еліпс

### Опис

```methodsynopsis
public ImagickDraw::ellipse(    float $ox,    float $oy,    float $rx,    float $ry,    float $start,    float $end): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює на зображенні еліпс.

### Список параметрів

`ox`

`oy`

`rx`

`ry`

`start`

`end`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::ellipse()\*\*\*\*

```php
<?php
function ellipse($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    $draw->ellipse(125, 70, 100, 50, 0, 360);
    $draw->ellipse(350, 70, 100, 50, 0, 315);

    $draw->push();
    $draw->translate(125, 250);
    $draw->rotate(30);
    $draw->ellipse(0, 0, 100, 50, 0, 360);
    $draw->pop();

    $draw->push();
    $draw->translate(350, 250);
    $draw->rotate(30);
    $draw->ellipse(0, 0, 100, 50, 0, 315);
    $draw->pop();

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
