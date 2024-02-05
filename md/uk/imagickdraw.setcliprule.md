---
navigation:
  - imagickdraw.setclippath.md: '« ImagickDraw::setClipPath'
  - imagickdraw.setclipunits.md: 'ImagickDraw::setClipUnits »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setClipRule'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setClipRule

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setClipRule — Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур

### Опис

```methodsynopsis
public ImagickDraw::setClipRule(int $fill_rule): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює правило заливання багатокутника, яке використовуватиметься відсічний контур.

### Список параметрів

`fill_rule`

Одна из констант[FILLRULE](imagick.constants.md#imagick.constants.fillrule) `imagick::FILLRULE_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setClipRule()\*\*\*\*

```php
<?php
function setClipRule($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);
    //\Imagick::FILLRULE_EVENODD
    //\Imagick::FILLRULE_NONZERO

    $clipPathName = 'testClipPath';
    $draw->pushClipPath($clipPathName);
    $draw->setClipRule(\Imagick::FILLRULE_EVENODD);
    $draw->rectangle(0, 0, 300, 500);
    $draw->rectangle(200, 0, 500, 500);
    $draw->popClipPath();
    $draw->setClipPath($clipPathName);
    $draw->rectangle(200, 200, 300, 300);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
