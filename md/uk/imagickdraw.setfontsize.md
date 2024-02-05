---
navigation:
  - imagickdraw.setfontfamily.md: '« ImagickDraw::setFontFamily'
  - imagickdraw.setfontstretch.md: 'ImagickDraw::setFontStretch »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFontSize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFontSize

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontSize — Встановлює розмір шрифту для використання при анотуванні текстом

### Опис

```methodsynopsis
public ImagickDraw::setFontSize(float $pointsize): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює розмір шрифту для використання під час анотування текстом.

### Список параметрів

`pointsize`

Розмір шрифту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setFontSize()\*\*\*\*

```php
<?php
function setFontSize($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFont("../fonts/Arial.ttf");

    $sizes = [24, 36, 48, 60, 72];

    foreach ($sizes as $size) {
        $draw->setFontSize($size);
        $draw->annotation(50, ($size * $size / 16), "Lorem Ipsum!");
    }

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
