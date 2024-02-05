---
navigation:
  - imagickdraw.settextalignment.md: '« ImagickDraw::setTextAlignment'
  - imagickdraw.settextdecoration.md: 'ImagickDraw::setTextDecoration »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setTextAntialias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setTextAntialias

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextAntialias — Керує згладжуванням тексту

### Опис

```methodsynopsis
public ImagickDraw::setTextAntialias(bool $antiAlias): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Керує згладжуванням тексту. За промовчанням текст згладжується.

### Список параметрів

`antiAlias`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setTextAntialias()\*\*\*\*

```php
<?php
function setTextAntialias($fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor('none');
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setFontSize(32);
    $draw->setTextAntialias(false);
    $draw->annotation(5, 30, "Lorem Ipsum!");
    $draw->setTextAntialias(true);
    $draw->annotation(5, 65, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(220, 80, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    //Scale the image so that people can see the aliasing.
    $imagick->scaleImage(220 * 6, 80 * 6);
    $imagick->cropImage(640, 480, 0, 0);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
