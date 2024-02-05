---
navigation:
  - imagickdraw.popclippath.md: '« ImagickDraw::popClipPath'
  - imagickdraw.poppattern.md: 'ImagickDraw::popPattern »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::popDefs'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::popDefs

(PECL imagick 2, PECL imagick 3)

ImagickDraw::popDefs — Завершує список визначень

### Опис

```methodsynopsis
public ImagickDraw::popDefs(): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Завершує перелік визначень.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::popDefs()\*\*\*\*

```php
<?php
function popDefs($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setstrokeOpacity(1);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);
    $draw->pushDefs();
    $draw->setStrokeColor('white');
    $draw->rectangle(50, 50, 200, 200);
    $draw->popDefs();

    $draw->rectangle(300, 50, 450, 200);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
