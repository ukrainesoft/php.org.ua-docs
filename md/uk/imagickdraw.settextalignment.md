---
navigation:
  - imagickdraw.setstrokewidth.md: '« ImagickDraw::setStrokeWidth'
  - imagickdraw.settextantialias.md: 'ImagickDraw::setTextAntialias »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setTextAlignment'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setTextAlignment

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextAlignment — Задає вирівнювання тексту

### Опис

```methodsynopsis
public ImagickDraw::setTextAlignment(int $alignment): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Визначає вирівнювання тексту, яке буде застосовуватися при анотуванні текстом.

### Список параметрів

`alignment`

Одна из констант[ALIGN](imagick.constants.md#imagick.constants.align) `imagick::ALIGN_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setTextAlignment()\*\*\*\*

```php
<?php
function setTextAlignment($strokeColor, $fillColor, $backgroundColor) {
    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setFontSize(36);

    $draw->setTextAlignment(\Imagick::ALIGN_LEFT);
    $draw->annotation(250, 75, "Lorem Ipsum!");
    $draw->setTextAlignment(\Imagick::ALIGN_CENTER);
    $draw->annotation(250, 150, "Lorem Ipsum!");
    $draw->setTextAlignment(\Imagick::ALIGN_RIGHT);
    $draw->annotation(250, 225, "Lorem Ipsum!");
    $draw->line(250, 0, 250, 500);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
