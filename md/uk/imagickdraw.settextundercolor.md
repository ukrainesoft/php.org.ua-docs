---
navigation:
  - imagickdraw.settextkerning.md: '« ImagickDraw::setTextKerning'
  - imagickdraw.setvectorgraphics.md: 'ImagickDraw::setVectorGraphics »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setTextUnderColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setTextUnderColor

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextUnderColor — Задає колір прямокутника тла.

### Опис

```methodsynopsis
public ImagickDraw::setTextUnderColor(ImagickPixel $under_color): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає колір прямокутника для розміщення під текстовими анотаціями.

### Список параметрів

`under_color`

Фоновий колір.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setTextUnderColor()\*\*\*\*

```php
<?php
function setTextUnderColor($strokeColor, $fillColor, $backgroundColor, $textUnderColor) {
    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);
    $draw->annotation(50, 75, "Lorem Ipsum!");
    $draw->setTextUnderColor($textUnderColor);
    $draw->annotation(50, 175, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
