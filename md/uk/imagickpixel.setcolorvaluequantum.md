---
navigation:
  - imagickpixel.setcolorvalue.md: '« ImagickPixel::setColorValue'
  - imagickpixel.sethsl.md: 'ImagickPixel::setHSL »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::setColorValueQuantum'
---
# ImagickPixel::setColorValueQuantum

(PECL imagick 2> = 2.3.0, PECL imagick 3)

ImagickPixel::setColorValueQuantum — Опис

### Опис

```methodsynopsis
public ImagickPixel::setColorValueQuantum(int $color, int|float $value): bool
```

Встановлює квантове значення колірного елемента ImagickPixel.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`color`

Який колірний елемент встановити, наприклад, Imagick::COLORGREEN.

`value`

Квантове значення елемента кольору. Це має бути число з плаваючою точкою, якщо ImageMagick був скомпільований з HDRI, інакше ціле число в діапазоні від 0 до Imagick::getQuantum().

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickPixel::setColorValueQuantum()****

```php
<?php
function setColorValueQuantum() {
    $image = new \Imagick();

    $quantumRange = $image->getQuantumRange();

    $draw = new \ImagickDraw();
    $color = new \ImagickPixel('blue');
    $color->setcolorValueQuantum(\Imagick::COLOR_RED, 128 * $quantumRange['quantumRangeLong'] / 256);

    $draw->setstrokewidth(1.0);
    $draw->setStrokeColor($color);
    $draw->setFillColor($color);
    $draw->rectangle(200, 200, 300, 300);

    $image->newImage(500, 500, "SteelBlue2");
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
