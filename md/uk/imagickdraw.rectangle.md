---
navigation:
  - imagickdraw.pushpattern.md: '« ImagickDraw::pushPattern'
  - imagickdraw.render.md: 'ImagickDraw::render »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::rectangle'
---
# ImagickDraw::rectangle

(PECL imagick 2, PECL imagick 3)

ImagickDraw::rectangle — Малює прямокутник

### Опис

```methodsynopsis
public ImagickDraw::rectangle(    float $x1,    float $y1,    float $x2,    float $y2): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює прямокутник по двох координатах за допомогою поточних параметрів обведення, ширини обведення та заливки.

### Список параметрів

`x1`

Координата x лівого верхнього кута.

`y1`

Координата у лівого верхнього кута.

`x2`

Координата x правого нижнього кута.

`y2`

Координата y правого нижнього кута.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::rectangle()****

```php
<?php
function rectangle($strokeColor, $fillColor, $backgroundColor) {
    $draw = new \ImagickDraw();
    $strokeColor = new \ImagickPixel($strokeColor);
    $fillColor = new \ImagickPixel($fillColor);

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeWidth(2);

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
