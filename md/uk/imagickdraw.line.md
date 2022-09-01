---
navigation:
  - imagickdraw.getvectorgraphics.md: '« ImagickDraw::getVectorGraphics'
  - imagickdraw.matte.md: 'ImagickDraw::matte »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::line'
---
# ImagickDraw::line

(PECL imagick 2, PECL imagick 3)

ImagickDraw::line — Малює лінію

### Опис

```methodsynopsis
public ImagickDraw::line(    float $sx,    float $sy,    float $ex,    float $ey): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює лінію на зображенні, використовуючи поточний колір обведення, прозорість і ширину.

### Список параметрів

`sx`

Початкова координата x.

`sy`

Початкова координата y.

`ex`

Кінцева координата x.

`ey`

Кінцева координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::line()****

```php
<?php
function line($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    $draw->line(125, 70, 100, 50);
    $draw->line(350, 170, 100, 150);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
