---
navigation:
  - imagickdraw.setresolution.md: '« ImagickDraw::setResolution'
  - imagickdraw.setstrokeantialias.md: 'ImagickDraw::setStrokeAntialias »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeAlpha'
---
# ImagickDraw::setStrokeAlpha

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeAlpha — Визначає непрозорість обведення контурів об'єкта

### Опис

```methodsynopsis
public ImagickDraw::setStrokeAlpha(float $opacity): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Визначає непрозорість обведення контурів об'єкта.

### Список параметрів

`opacity`

Непрозорість.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setStrokeAlpha()****

```php
<?php
function setStrokeAlpha($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(4);
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
