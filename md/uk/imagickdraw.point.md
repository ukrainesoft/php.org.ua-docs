---
navigation:
  - imagickdraw.pathstart.md: '« ImagickDraw::pathStart'
  - imagickdraw.polygon.md: 'ImagickDraw::polygon »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::point'
---
# ImagickDraw::point

(PECL imagick 2, PECL imagick 3)

ImagickDraw::point — Малює точку

### Опис

```methodsynopsis
public ImagickDraw::point(float $x, float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює точку, використовуючи поточний колір та товщину обведення за вказаними координатами.

### Список параметрів

`x`

Координата x.

`y`

Координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::point()****

```php
<?php
function point($fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setFillColor($fillColor);

    for ($x = 0; $x < 10000; $x++) {
        $draw->point(rand(0, 500), rand(0, 500));
    }

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
