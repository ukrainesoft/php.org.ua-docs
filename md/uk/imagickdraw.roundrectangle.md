---
navigation:
  - imagickdraw.rotate.md: '« ImagickDraw::rotate'
  - imagickdraw.scale.md: 'ImagickDraw::scale »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::roundRectangle'
---
# ImagickDraw::roundRectangle

(PECL imagick 2, PECL imagick 3)

ImagickDraw::roundRectangle — Малює прямокутник із закругленими кутами.

### Опис

```methodsynopsis
public ImagickDraw::roundRectangle(    float $x1,    float $y1,    float $x2,    float $y2,    float $rx,    float $ry): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює прямокутник із закругленими кутами за двома координатами та радіусами кутів x & y, використовуючи поточне обведення, її ширину та налаштування заливки.

### Список параметрів

`x1`

Координата x лівого верхнього кута.

`y1`

Координата у лівого верхнього кута.

`x2`

Координата x правого нижнього кута.

`y2`

Координата y правого нижнього кута.

`rx`

Округлення по осі x.

`ry`

Округлення по осі y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::roundRectangle()****

```php
<?php
function roundRectangle($strokeColor, $fillColor, $backgroundColor, $startX, $startY, $endX, $endY, $roundX, $roundY) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);

    $draw->roundRectangle($startX, $startY, $endX, $endY, $roundX, $roundY);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
