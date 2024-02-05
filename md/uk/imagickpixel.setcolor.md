---
navigation:
  - imagickpixel.issimilar.md: '« ImagickPixel::isSimilar'
  - imagickpixel.setcolorcount.md: 'ImagickPixel::setColorCount »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::setColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::setColor

(PECL imagick 2, PECL imagick 3)

ImagickPixel::setColor — Встановлює колір

### Опис

```methodsynopsis
public ImagickPixel::setColor(string $color): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює колір об'єкта ImagickPixel зазначеним рядком (наприклад, "blue", "#0000ff", "rgb(0,0,255)", "cmyk(100,100,100,10)" і т.д.).

### Список параметрів

`color`

Визначення кольору для використання в порядку ініціалізації об'єкту ImagickPixel.

### Значення, що повертаються

Повертає **`true`** якщо колір був встановлений, інакше **`false`**

### Приклади

**Приклад #1 Приклад використання** ImagickPixel::setColor()\*\*\*\*

```php
<?php
function setColor() {
    $draw = new \ImagickDraw();

    $strokeColor = new \ImagickPixel('green');
    $fillColor = new \ImagickPixel();
    $fillColor->setColor('rgba(100%, 75%, 0%, 1.0)');

    $draw->setstrokewidth(3.0);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->rectangle(200, 200, 300, 300);

    $image = new \Imagick();
    $image->newImage(500, 500, "SteelBlue2");
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
