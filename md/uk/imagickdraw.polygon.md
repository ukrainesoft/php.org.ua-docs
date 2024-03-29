---
navigation:
  - imagickdraw.point.md: '« ImagickDraw::point'
  - imagickdraw.polyline.md: 'ImagickDraw::polyline »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::polygon'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::polygon

(PECL imagick 2, PECL imagick 3)

ImagickDraw::polygon — Малює багатокутник.

### Опис

```methodsynopsis
public ImagickDraw::polygon(array $coordinates): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Малює багатокутник з використанням поточного обведення, його ширини, кольору заливки або текстури з використанням вказаного масиву координат.

### Список параметрів

`coordinates`

Багатомірний масив на кшталт array( array( 'x' => 3, 'y' => 4 ), array( 'x' => 2, 'y' => 6 ) );

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::polygon()\*\*\*\*

```php
<?php
function polygon($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(4);

    $draw->setFillColor($fillColor);

    $points = [
        ['x' => 40 * 5, 'y' => 10 * 5],
        ['x' => 20 * 5, 'y' => 20 * 5],
        ['x' => 70 * 5, 'y' => 50 * 5],
        ['x' => 60 * 5, 'y' => 15 * 5],
    ];

    $draw->polygon($points);

    $image = new \Imagick();
    $image->newImage(500, 300, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
