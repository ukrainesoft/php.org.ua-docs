---
navigation:
  - imagickpixel.clear.md: '« ImagickPixel::clear'
  - imagickpixel.destroy.md: 'ImagickPixel::destroy »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::\_\_construct

(PECL imagick 2, PECL imagick 3)

ImagickPixel::\_\_construct — Конструктор ImagickPixel

### Опис

```methodsynopsis
public ImagickPixel::__construct(string $color = ?)
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Створюється об'єкт ImagickPixel. Якщо вказано колір, об'єкт створюється та ініціалізується з цим кольором перед поверненням.

### Список параметрів

`color`

Необов'язковий рядок із кольором для використання в ініціалізації цього об'єкта.

### Значення, що повертаються

У разі успішного виконання повертає об'єкт ImagickPixel, інакше викидає виняток ImagickPixelException.

### Приклади

**Приклад #1 Приклад використання** ImagickPixel::construct()\*\*\*\*

```php
<?php
function construct() {

    $columns = 4;

    $exampleColors = array(
        "rgba(100%, 0%, 0%, 0.5)",
        "hsb(33.3333%, 100%,  75%)", // medium green
        "hsl(120, 255,   191.25)", //medium green
        "graya(50%, 0.5)", //  semi-transparent mid gray
        "LightCoral", "none", //"cmyk(0.9, 0.48, 0.83, 0.50)",
        "#f00", //  #rgb
        "#ff0000", //  #rrggbb
        "#ff0000ff", //  #rrggbbaa
        "#ffff00000000", //  #rrrrggggbbbb
        "#ffff00000000ffff", //  #rrrrggggbbbbaaaa
        "rgb(255, 0, 0)", //  an integer in the range 0—255 for each component
        "rgb(100.0%, 0.0%, 0.0%)", //  a float in the range 0—100% for each component
        "rgb(255, 0, 0)", //  range 0 - 255
        "rgba(255, 0, 0, 1.0)", //  the same, with an explicit alpha value
        "rgb(100%, 0%, 0%)", //  range 0.0% - 100.0%
        "rgba(100%, 0%, 0%, 1.0)", //  the same, with an explicit alpha value
    );

    $draw = new \ImagickDraw();
    $count = 0;
    $black = new \ImagickPixel('rgb(0, 0, 0)');

    foreach ($exampleColors as $exampleColor) {
        $color = new \ImagickPixel($exampleColor);

        $draw->setstrokewidth(1.0);
        $draw->setStrokeColor($black);
        $draw->setFillColor($color);
        $offsetX = ($count % $columns) * 50 + 5;
        $offsetY = intval($count / $columns) * 50 + 5;
        $draw->rectangle(0 + $offsetX, 0 + $offsetY, 40 + $offsetX, 40 + $offsetY);
        $count++;
    }

    $image = new \Imagick();
    $image->newImage(350, 350, "blue");
    $image->setImageFormat("png");
    $image->drawImage($draw);
    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
