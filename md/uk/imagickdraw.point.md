---
navigation:
  - imagickdraw.pathstart.md: '« ImagickDraw::pathStart'
  - imagickdraw.polygon.md: 'ImagickDraw::polygon »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::point'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::point

(PECL imagick 2, PECL imagick 3)

ImagickDraw::point — Малює точку

### Опис

```methodsynopsis
public ImagickDraw::point(float $x, float $y): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює точку, використовуючи поточний колір та товщину обведення за вказаними координатами.

### Список параметрів

`x`

Координата x.

`y`

Координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**ImagickDraw::point()\*\*\*\*

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
