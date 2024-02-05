---
navigation:
  - imagickdraw.setclipunits.md: '« ImagickDraw::setClipUnits'
  - imagickdraw.setfillcolor.md: 'ImagickDraw::setFillColor »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFillAlpha'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFillAlpha

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillAlpha — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.

### Опис

```methodsynopsis
public ImagickDraw::setFillAlpha(float $opacity): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює непрозорість при малюванні за допомогою кольору або текстури заливки. Повністю непрозорий – 1.0.

### Список параметрів

`opacity`

Непрозорість заливання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setFillAlpha()\*\*\*\*

```php
<?php
function setFillAlpha($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);
    $draw->rectangle(100, 200, 200, 300);
    @$draw->setFillAlpha(0.4);
    $draw->rectangle(300, 200, 400, 300);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
