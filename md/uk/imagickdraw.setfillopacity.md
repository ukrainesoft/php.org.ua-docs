---
navigation:
  - imagickdraw.setfillcolor.md: '« ImagickDraw::setFillColor'
  - imagickdraw.setfillpatternurl.md: 'ImagickDraw::setFillPatternURL »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setFillOpacity'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setFillOpacity

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillOpacity — Встановлює непрозорість під час малювання за допомогою кольору або текстури заливки.

### Опис

```methodsynopsis
public ImagickDraw::setFillOpacity(float $fillOpacity): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює непрозорість при малюванні за допомогою кольору або текстури заливки. Повністю непрозорий – 1.0.

### Список параметрів

`fillOpacity`

Непрозорість заливання.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setFillOpacity()\*\*\*\*

```php
<?php
function setFillOpacity($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);

    $draw->rectangle(100, 200, 200, 300);

    $draw->setFillOpacity(0.4);
    $draw->rectangle(300, 200, 400, 300);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
