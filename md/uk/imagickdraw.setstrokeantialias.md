---
navigation:
  - imagickdraw.setstrokealpha.md: '« ImagickDraw::setStrokeAlpha'
  - imagickdraw.setstrokecolor.md: 'ImagickDraw::setStrokeColor »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeAntialias'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeAntialias

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeAntialias — Керує згладжуванням обведення контурів

### Опис

```methodsynopsis
public ImagickDraw::setStrokeAntialias(bool $stroke_antialias): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Керує згладжуванням обведення контурів. За промовчанням обведені контури згладжуються. Коли згладжування вимкнено, для обведених пікселів встановлюється граничне значення, щоб визначити, чи слід використовувати колір обведення або колір базового полотна.

### Список параметрів

`stroke_antialias`

Налаштування згладжування.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setStrokeAntialias()\*\*\*\*

```php
<?php
function setStrokeAntialias($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setStrokeAntialias(false);
    $draw->line(100, 100, 400, 105);

    $draw->line(100, 140, 400, 185);

    $draw->setStrokeAntialias(true);
    $draw->line(100, 110, 400, 115);
    $draw->line(100, 150, 400, 195);

    $image = new \Imagick();
    $image->newImage(500, 250, $backgroundColor);
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
