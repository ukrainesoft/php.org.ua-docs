---
navigation:
  - imagickkernel.frombuiltin.md: '« ImagickKernel::fromBuiltIn'
  - imagickkernel.getmatrix.md: 'ImagickKernel::getMatrix »'
  - index.md: PHP Manual
  - class.imagickkernel.md: ImagickKernel
title: 'ImagickKernel::fromMatrix'
---
# ImagickKernel::fromMatrix

(PECL imagick >= 3.3.0)

ImagickKernel::fromMatrix — Опис

### Опис

```methodsynopsis
public static ImagickKernel::fromMatrix(array $matrix, array $origin = ?): ImagickKernel
```

Створює ядро ​​двомерної матриці значень. Кожне значення має бути або числом з плаваючою комою (якщо елемент повинен використовуватися), або з false, якщо елемент слід пропустити. Для матриць непарних розмірів в обох вимірах вихідним пікселем за промовчанням буде центр ядра. Для інших розмірів ядра необхідно вказати вихідний піксель.

### Список параметрів

`array`

Матриця (тобто двовимірний масив) значень, що визначають ядро. Кожен елемент повинен бути або числом з плаваючою комою або значенням FALSE, якщо цей елемент не повинен використовуватися ядром.

`array`

Який елемент ядра слід використовувати як вихідний піксель. Наприклад, для матриці 3x3, що визначає початок координат як , буде вказано, що нижній правий елемент має бути вихідним пікселем.

### Значення, що повертаються

Створений ImagickKernel.

### Приклади

**Приклад #1 Приклад використання **ImagickKernel::fromMatrix()****

```php
<?php

function renderKernel(ImagickKernel $imagickKernel) {
    $matrix = $imagickKernel->getMatrix();

    $imageMargin = 20;

    $tileSize = 20;
    $tileSpace = 4;
    $shadowSigma = 4;
    $shadowDropX = 20;
    $shadowDropY = 0;

    $radius = ($tileSize / 2) * 0.9;

    $rows = count($matrix);
    $columns = count($matrix[0]);

    $imagickDraw = new \ImagickDraw();

    $imagickDraw->setFillColor('#afafaf');
    $imagickDraw->setStrokeColor('none');

    $imagickDraw->translate($imageMargin, $imageMargin);
    $imagickDraw->push();

    ksort($matrix);

    foreach ($matrix as $row) {
        ksort($row);
        $imagickDraw->push();
        foreach ($row as $cell) {
            if ($cell !== false) {
                $color = intval(255 * $cell);
                $colorString = sprintf("rgb(%f, %f, %f)", $color, $color, $color);
                $imagickDraw->setFillColor($colorString);
                $imagickDraw->rectangle(0, 0, $tileSize, $tileSize);
            }
            $imagickDraw->translate(($tileSize + $tileSpace), 0);
        }
        $imagickDraw->pop();
        $imagickDraw->translate(0, ($tileSize + $tileSpace));
    }

    $imagickDraw->pop();

    $width = ($columns * $tileSize) + (($columns - 1) * $tileSpace);
    $height = ($rows * $tileSize) + (($rows - 1) * $tileSpace);

    $imagickDraw->push();
    $imagickDraw->translate($width/2 , $height/2);
    $imagickDraw->setFillColor('rgba(0, 0, 0, 0)');
    $imagickDraw->setStrokeColor('white');
    $imagickDraw->circle(0, 0, $radius - 1, 0);
    $imagickDraw->setStrokeColor('black');
    $imagickDraw->circle(0, 0, $radius, 0);
    $imagickDraw->pop();

    $canvasWidth = $width + (2 * $imageMargin);
    $canvasHeight = $height + (2 * $imageMargin);

    $kernel = new \Imagick();
    $kernel->newPseudoImage(
        $canvasWidth,
        $canvasHeight,
        'canvas:none'
    );

    $kernel->setImageFormat('png');
    $kernel->drawImage($imagickDraw);

    /* создание тени на собственном слое */
    $canvas = $kernel->clone();
    $canvas->setImageBackgroundColor(new \ImagickPixel('rgb(0, 0, 0)'));
    $canvas->shadowImage(100, $shadowSigma, $shadowDropX, $shadowDropY);

    $canvas->setImagePage($canvasWidth, $canvasHeight, -5, -5);
    $canvas->cropImage($canvasWidth, $canvasHeight, 0, 0);

    /* накладывает исходный text_layer на shadow_layer */
    $canvas->compositeImage($kernel, \Imagick::COMPOSITE_OVER, 0, 0);
    $canvas->setImageFormat('png');

    return $canvas;
}

function createFromMatrix() {
    $matrix = [
        [0.5, 0, 0.2],
        [0, 1, 0],
        [0.9, 0, false],
    ];

    $kernel = \ImagickKernel::fromMatrix($matrix);

    return $kernel;
}

function fromMatrix() {
    $kernel = createFromMatrix();
    $imagick = renderKernel($kernel);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
