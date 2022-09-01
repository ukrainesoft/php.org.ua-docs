---
navigation:
  - imagickdraw.setfontfamily.html: '« ImagickDraw::setFontFamily'
  - imagickdraw.setfontstretch.html: 'ImagickDraw::setFontStretch »'
  - index.html: PHP Manual
  - class.imagickdraw.html: ImagickDraw
title: 'ImagickDraw::setFontSize'
---
# ImagickDraw::setFontSize

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontSize — Встановлює розмір шрифту для використання при анотуванні текстом

### Опис

```methodsynopsis
public ImagickDraw::setFontSize(float $pointsize): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює розмір шрифту для використання під час анотування текстом.

### Список параметрів

`pointsize`

Розмір шрифту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setFontSize()****

```php
<?php
function setFontSize($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFont("../fonts/Arial.ttf");

    $sizes = [24, 36, 48, 60, 72];

    foreach ($sizes as $size) {
        $draw->setFontSize($size);
        $draw->annotation(50, ($size * $size / 16), "Lorem Ipsum!");
    }

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
