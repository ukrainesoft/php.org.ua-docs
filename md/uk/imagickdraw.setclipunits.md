---
navigation:
  - imagickdraw.setcliprule.md: '« ImagickDraw::setClipRule'
  - imagickdraw.setfillalpha.md: 'ImagickDraw::setFillAlpha »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setClipUnits'
---
# ImagickDraw::setClipUnits

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setClipUnits — Встановлює інтерпретацію одиниць траєкторії відсічного контуру

### Опис

```methodsynopsis
public ImagickDraw::setClipUnits(int $clip_units): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює інтерпретацію одиниць траєкторії відсічного контуру.

### Список параметрів

`clip_units`

кількість одиниць відсічного контуру

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setClipUnits()****

```php
<?php
function setClipUnits($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);
    $clipPathName = 'testClipPath';
    $draw->setClipUnits(\Imagick::RESOLUTION_PIXELSPERINCH);
    $draw->pushClipPath($clipPathName);
    $draw->rectangle(0, 0, 250, 250);
    $draw->popClipPath();
    $draw->setClipPath($clipPathName);

    //RESOLUTION_PIXELSPERINCH
    //RESOLUTION_PIXELSPERCENTIMETER

    $draw->rectangle(200, 200, 300, 300);
    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
