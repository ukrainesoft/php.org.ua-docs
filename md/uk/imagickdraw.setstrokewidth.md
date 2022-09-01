---
navigation:
  - imagickdraw.setstrokepatternurl.html: '« ImagickDraw::setStrokePatternURL'
  - imagickdraw.settextalignment.html: 'ImagickDraw::setTextAlignment »'
  - index.html: PHP Manual
  - class.imagickdraw.html: ImagickDraw
title: 'ImagickDraw::setStrokeWidth'
---
# ImagickDraw::setStrokeWidth

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeWidth — Встановлює ширину обведення, яка використовується для малювання контурів об'єкта.

### Опис

```methodsynopsis
public ImagickDraw::setStrokeWidth(float $stroke_width): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює ширину обведення для малювання контурів об'єкта.

### Список параметрів

`stroke_width`

Ширина обведення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setStrokeWidth()****

```php
<?php
function setStrokeWidth($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeWidth(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->line(100, 100, 400, 145);
    $draw->rectangle(100, 200, 225, 350);
    $draw->setStrokeWidth(5);
    $draw->line(100, 120, 400, 165);
    $draw->rectangle(275, 200, 400, 350);

    $image = new \Imagick();
    $image->newImage(500, 400, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
