---
navigation:
  - imagickdraw.scale.md: '« ImagickDraw::scale'
  - imagickdraw.setcliprule.md: 'ImagickDraw::setClipRule »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setClipPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setClipPath

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setClipPath — Зв'язує іменований контур відсічного контуру із зображенням

### Опис

```methodsynopsis
public ImagickDraw::setClipPath(string $clip_mask): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Зв'язує іменований контур відсічного контуру із зображенням. Тільки області, намальовані відсічний контур, будуть змінені, поки він залишається в силі.

### Список параметрів

`clip_mask`

ім'я відсічного контуру

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::setClipPath()\*\*\*\*

```php
<?php
function setClipPath($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);

    $clipPathName = 'testClipPath';

    $draw->pushClipPath($clipPathName);
    $draw->rectangle(0, 0, 250, 250);
    $draw->popClipPath();
    $draw->setClipPath($clipPathName);
    $draw->rectangle(100, 100, 400, 400);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
