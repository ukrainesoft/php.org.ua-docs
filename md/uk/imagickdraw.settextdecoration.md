---
navigation:
  - imagickdraw.settextantialias.md: '« ImagickDraw::setTextAntialias'
  - imagickdraw.settextencoding.md: 'ImagickDraw::setTextEncoding »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setTextDecoration'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setTextDecoration

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextDecoration — Визначає оформлення

### Опис

```methodsynopsis
public ImagickDraw::setTextDecoration(int $decoration): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає оформлення, яке застосовуватиметься при анотуванні текстом.

### Список параметрів

`decoration`

Одна из констант[DECORATION](imagick.constants.md#imagick.constants.decoration) `imagick::DECORATION_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setTextDecoration()\*\*\*\*

```php
<?php
function setTextDecoration($strokeColor, $fillColor, $backgroundColor, $textDecoration) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);
    $draw->setTextDecoration($textDecoration);
    $draw->annotation(50, 75, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(500, 200, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
