---
navigation:
  - imagickdraw.setstrokedasharray.md: '« ImagickDraw::setStrokeDashArray'
  - imagickdraw.setstrokelinecap.md: 'ImagickDraw::setStrokeLineCap »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::setStrokeDashOffset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::setStrokeDashOffset

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeDashOffset — Задає зміщення в штриховому патерні для початку штрихування

### Опис

```methodsynopsis
public ImagickDraw::setStrokeDashOffset(float $dash_offset): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Задає усунення в штриховому патерні для початку штрихування.

### Список параметрів

`dash_offset`

Зміщення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::setStrokeDashOffset()\*\*\*\*

```php
<?php
function setStrokeDashOffset($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(4);
    $draw->setStrokeDashArray([20, 20]);
    $draw->setStrokeDashOffset(0);
    $draw->rectangle(100, 50, 225, 175);

    //Начало эффекта штриховки в середине сплошной части
    $draw->setStrokeDashOffset(10);
    $draw->rectangle(275, 50, 400, 175);

    //Начало эффекта штриховки в пространственной части
    $draw->setStrokeDashOffset(20);
    $draw->rectangle(100, 200, 225, 350);
    $draw->setStrokeDashOffset(5);
    $draw->rectangle(275, 200, 400, 350);

    $image = new \Imagick();
    $image->newImage(500, 400, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
