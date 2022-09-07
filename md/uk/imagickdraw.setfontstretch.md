---
navigation:
  - imagickdraw.setfontsize.md: '« ImagickDraw::setFontSize'
  - imagickdraw.setfontstyle.md: 'ImagickDraw::setFontStyle »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFontStretch'
---
# ImagickDraw::setFontStretch

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontStretch — Встановлює розтягування шрифту для використання при анотуванні текстом

### Опис

```methodsynopsis
public ImagickDraw::setFontStretch(int $fontStretch): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює розтягування шрифту для використання під час анотування текстом. Використання AnyStretch діє як "будь-яке".

### Список параметрів

`fontStretch`

Одна з констант [STRETCH](imagick.constants.md#imagick.constants.stretch) `imagick::STRETCH_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setFontStretch()****

```php
<?php
function setFontStretch($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(36);

    $fontStretchTypes = [
        \Imagick::STRETCH_ULTRACONDENSED,
        \Imagick::STRETCH_CONDENSED,
        \Imagick::STRETCH_SEMICONDENSED,
        \Imagick::STRETCH_SEMIEXPANDED,
        \Imagick::STRETCH_EXPANDED,
        \Imagick::STRETCH_EXTRAEXPANDED,
        \Imagick::STRETCH_ULTRAEXPANDED,
        \Imagick::STRETCH_ANY
    ];

    $offset = 0;
    foreach ($fontStretchTypes as $fontStretch) {
        $draw->setFontStretch($fontStretch);
        $draw->annotation(50, 75 + $offset, "Lorem Ipsum!");
        $offset += 50;
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
