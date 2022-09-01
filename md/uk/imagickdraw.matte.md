---
navigation:
  - imagickdraw.line.html: '« ImagickDraw::line'
  - imagickdraw.pathclose.html: 'ImagickDraw::pathClose »'
  - index.html: PHP Manual
  - class.imagickdraw.html: ImagickDraw
title: 'ImagickDraw::matte'
---
# ImagickDraw::matte

(PECL imagick 2, PECL imagick 3)

ImagickDraw::matte — Зафарбовує канал непрозорості зображення

### Опис

```methodsynopsis
public ImagickDraw::matte(float $x, float $y, int $paintMethod): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Зафарбовує канал непрозорості зображення з метою зробити торкнуті пікселі прозорими.

### Список параметрів

`x`

Координата x.

`y`

Координата y.

`paintMethod`

Одна з констант [PAINT](imagick.constants.html#imagick.constants.paint) `imagick::PAINT_*`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::matte()****

```php
<?php
function matte($strokeColor, $fillColor, $backgroundColor, $paintType) {
    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    $draw->matte(120, 120, $paintType);
    $draw->rectangle(100, 100, 300, 200);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
