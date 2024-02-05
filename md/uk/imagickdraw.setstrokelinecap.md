---
navigation:
  - imagickdraw.setstrokedashoffset.md: '« ImagickDraw::setStrokeDashOffset'
  - imagickdraw.setstrokelinejoin.md: 'ImagickDraw::setStrokeLineJoin »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeLineCap'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeLineCap

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeLineCap — Задає форму, яка буде використовуватися в кінці відкритих внутрішніх контурів під час їх обведення

### Опис

```methodsynopsis
public ImagickDraw::setStrokeLineCap(int $linecap): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає форму, яка використовуватиметься наприкінці відкритих внутрішніх контурів під час їх обведення.

### Список параметрів

`linecap`

Одна из констант[LINECAP](imagick.constants.md#imagick.constants.linecap) `imagick::LINECAP_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setStrokeLineCap()\*\*\*\*

```php
<?php
function setStrokeLineCap($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(25);

    $lineTypes = [\Imagick::LINECAP_BUTT, \Imagick::LINECAP_ROUND, \Imagick::LINECAP_SQUARE,];

    $offset = 0;

    foreach ($lineTypes as $lineType) {
        $draw->setStrokeLineCap($lineType);
        $draw->line(50 + $offset, 50, 50 + $offset, 250);
        $offset += 50;
    }

    $imagick = new \Imagick();
    $imagick->newImage(300, 300, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
