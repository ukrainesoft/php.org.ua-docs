---
navigation:
  - imagickdraw.setclippath.html: '« ImagickDraw::setClipPath'
  - imagickdraw.setclipunits.html: 'ImagickDraw::setClipUnits »'
  - index.html: PHP Manual
  - class.imagickdraw.html: ImagickDraw
title: 'ImagickDraw::setClipRule'
---
# ImagickDraw::setClipRule

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setClipRule — Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур

### Опис

```methodsynopsis
public ImagickDraw::setClipRule(int $fill_rule): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур.

### Список параметрів

`fill_rule`

Одна з констант [FILLRULE](imagick.constants.html#imagick.constants.fillrule) `imagick::FILLRULE_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setClipRule()****

```php
<?php
function setClipRule($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);
    //\Imagick::FILLRULE_EVENODD
    //\Imagick::FILLRULE_NONZERO

    $clipPathName = 'testClipPath';
    $draw->pushClipPath($clipPathName);
    $draw->setClipRule(\Imagick::FILLRULE_EVENODD);
    $draw->rectangle(0, 0, 300, 500);
    $draw->rectangle(200, 0, 500, 500);
    $draw->popClipPath();
    $draw->setClipPath($clipPathName);
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
