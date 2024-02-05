---
navigation:
  - imagickdraw.setfontstyle.md: '« ImagickDraw::setFontStyle'
  - imagickdraw.setgravity.md: 'ImagickDraw::setGravity »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFontWeight'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFontWeight

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontWeight — Встановлює товщину шрифту

### Опис

```methodsynopsis
public ImagickDraw::setFontWeight(int $font_weight): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює товщину шрифту для використання під час анотування текстом.

### Список параметрів

`font_weight`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setFontWeight()\*\*\*\*

```php
<?php
function setFontWeight($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(1);

    $draw->setFontSize(36);

    $draw->setFontWeight(100);
    $draw->annotation(50, 50, "Lorem Ipsum!");

    $draw->setFontWeight(200);
    $draw->annotation(50, 100, "Lorem Ipsum!");

    $draw->setFontWeight(400);
    $draw->annotation(50, 150, "Lorem Ipsum!");

    $draw->setFontWeight(800);
    $draw->annotation(50, 200, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
