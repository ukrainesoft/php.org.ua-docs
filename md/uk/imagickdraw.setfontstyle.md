---
navigation:
  - imagickdraw.setfontstretch.md: '« ImagickDraw::setFontStretch'
  - imagickdraw.setfontweight.md: 'ImagickDraw::setFontWeight »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFontStyle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFontStyle

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontStyle — Встановлює стиль шрифту для використання при анотуванні текстом

### Опис

```methodsynopsis
public ImagickDraw::setFontStyle(int $style): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює стиль шрифту, який буде використовуватися під час анотування тексту. Використання AnyStyle діє як "будь-який".

### Список параметрів

`style`

Одна из констант[STYLE](imagick.constants.md#imagick.constants.styles) `imagick::STYLE_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setFontStyle()\*\*\*\*

```php
<?php
function setFontStyle($fillColor, $strokeColor, $backgroundColor) {
    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setFontSize(36);
    $draw->setFontStyle(\Imagick::STYLE_NORMAL);
    $draw->annotation(50, 50, "Lorem Ipsum!");

    $draw->setFontStyle(\Imagick::STYLE_ITALIC);
    $draw->annotation(50, 100, "Lorem Ipsum!");

    $draw->setFontStyle(\Imagick::STYLE_OBLIQUE);
    $draw->annotation(50, 150, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(350, 300, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
