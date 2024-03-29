---
navigation:
  - imagickdraw.line.md: '« ImagickDraw::line'
  - imagickdraw.pathclose.md: 'ImagickDraw::pathClose »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::matte'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::matte

(PECL imagick 2, PECL imagick 3)

ImagickDraw::matte — Зафарбовує канал непрозорості зображення

### Опис

```methodsynopsis
public ImagickDraw::matte(float $x, float $y, int $paintMethod): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Зафарбовує канал непрозорості зображення з метою зробити торкнуті пікселі прозорими.

### Список параметрів

`x`

Координата x.

`y`

Координата y.

`paintMethod`

Одна из констант[PAINT](imagick.constants.md#imagick.constants.paint) `imagick::PAINT_*`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::matte()\*\*\*\*

```php
<?php
function matte($strokeColor, $fillColor, $backgroundColor, $paintType) {
    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    $draw->matte(120, 120, $paintType);
    $draw->rectangle(100, 100, 300, 200);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
