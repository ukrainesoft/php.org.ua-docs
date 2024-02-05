---
navigation:
  - imagickdraw.setfillalpha.md: '« ImagickDraw::setFillAlpha'
  - imagickdraw.setfillopacity.md: 'ImagickDraw::setFillOpacity »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFillColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFillColor

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillColor — Встановлює колір заливки, який використовується для малювання об'єктів із заливкою.

### Опис

```methodsynopsis
public ImagickDraw::setFillColor(ImagickPixel $fill_pixel): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює колір заливки для малювання об'єктів із заливкою.

### Список параметрів

`fill_pixel`

Об'єкт ImagickPixel, який використовується для встановлення кольору.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setFillColor()\*\*\*\*

```php
<?php
function setFillColor($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(1.5);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->rectangle(50, 50, 150, 150);

    $draw->setFillColor("rgb(200, 32, 32)");
    $draw->rectangle(200, 50, 300, 150);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
