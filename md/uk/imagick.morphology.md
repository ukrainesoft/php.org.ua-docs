---
navigation:
  - imagick.morphimages.html: '« Imagick::morphImages'
  - imagick.mosaicimages.html: 'Imagick::mosaicImages »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::morphology'
---
# Imagick::morphology

(PECL imagick 3> = 3.3.0)

Imagick::morphology — Опис

### Опис

```methodsynopsis
public Imagick::morphology(    int $morphologyMethod,    int $iterations,    ImagickKernel $ImagickKernel,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує зображення ядро, надане користувачем, відповідно до заданого методу морфології.

### Список параметрів

`morphologyMethod`

Який метод морфології використовувати: одна з констант Imagick::MORPHOLOGY

`iterations`

Кількість ітерацій до застосування морфологічної функції. Значення -1 означає цикл, доки не буде знайдено жодних змін. Як це застосовується, може залежати від методу морфології. Зазвичай це значення дорівнює 1.

`ImagickKernel`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання методу Convolve **Imagick::morphology()****

```php
<?php
$imagick = $this->getCharacter();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_GAUSSIAN, "5,1");
$imagick->morphology(\Imagick::MORPHOLOGY_CONVOLVE, 2, $kernel);
header("Content-Type: image/png");
echo $imagick->getImageBlob();

?>
```

**Приклад #2 Приклад використання методу Correlate **Imagick::morphology()****

```php
<?php
// Верхний левый пиксель должен быть чёрным.
// Нижний правый пиксель должен быть белым
// На остальное нам всё равно.

$imagick = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromMatrix(self::$correlateMatrix, [2, 2]);
$imagick->morphology(\Imagick::MORPHOLOGY_CORRELATE, 1, $kernel);
header("Content-Type: image/png");
echo $imagick->getImageBlob();

?>
```

**Приклад #3 Приклад використання методу Erode **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_ERODE, 2, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #4 Приклад використання методу Erode Intensity **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacter();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "1");
$canvas->morphology(\Imagick::MORPHOLOGY_ERODE_INTENSITY, 2, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #5 Приклад використання методу Dilate **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_DILATE, 4, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #6 Приклад використання методу Dilate intensity **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacter();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "1");
$canvas->morphology(\Imagick::MORPHOLOGY_DILATE_INTENSITY, 4, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #7 Приклад використання методу Distance із ядром Chebyshev **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_CHEBYSHEV, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_DISTANCE, 3, $kernel);
$canvas->autoLevelImage();
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #8 Приклад використання методу Distance із ядром Manhattan **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_MANHATTAN, "5");
$canvas->morphology(\Imagick::MORPHOLOGY_DISTANCE, 3, $kernel);
$canvas->autoLevelImage();
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #9 Приклад використання методу Distance з ядром ocatagonal **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGONAL, "5");
$canvas->morphology(\Imagick::MORPHOLOGY_DISTANCE, 3, $kernel);
$canvas->autoLevelImage();
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #10 Приклад використання методу Distance з ядром Euclidean **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_EUCLIDEAN, "4");
$canvas->morphology(\Imagick::MORPHOLOGY_DISTANCE, 3, $kernel);
$canvas->autoLevelImage();
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #11 Приклад використання методу Edge **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_EDGE, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #12 Приклад використання методу Open **Imagick::morphology()****

```php
<?php
// В результате вы увидите, что "Open" сглаживает контур, округляя все острые точки, и удаляет все части, которые меньше используемой формы.
// Он также отключит или откроет любые тонкие мосты.
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "6");
$canvas->morphology(\Imagick::MORPHOLOGY_OPEN, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #13 Приклад використання методу Open intensity **Imagick::morphology()****

```php
<?php
// В результате вы увидите, что "Open" сглаживает контур, округляя все острые точки, и удаляет все части, которые меньше используемой формы.
// Он также отключит или откроет любые тонкие мосты.

$canvas = $this->getCharacter();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "6");
$canvas->morphology(\Imagick::MORPHOLOGY_OPEN_INTENSITY, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #14 Приклад використання методу Close **Imagick::morphology()****

```php
<?php
// Основное использование метода "Close" - уменьшить или удалить любые дыры или пробелы в размере Структурного элемента ядра.
// Это "близкие" части фона примерно такого размера.
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "6");
$canvas->morphology(\Imagick::MORPHOLOGY_CLOSE, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #15 Приклад використання методу Close Intensity **Imagick::morphology()****

```php
<?php
// Основное использование метода "Close" - уменьшить или удалить любые дыры или пробелы в размере Структурного элемента ядра.
// Это "близкие" части фона примерно такого размера.
$canvas = $this->getCharacter();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "6");
$canvas->morphology(\Imagick::MORPHOLOGY_CLOSE_INTENSITY, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #16 Приклад використання методу Smooth **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_SMOOTH, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #17 Приклад використання методу Edge in **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_EDGE_IN, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #18 Приклад використання методу Edge out **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_OCTAGON, "3");
$canvas->morphology(\Imagick::MORPHOLOGY_EDGE_OUT, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #19 Метод "TopHat", або, точніше, "White TopHat", повертає пікселі, які були видалені відкриттям фігури, тобто пікселі, які були видалені для заокруглення крапок, та з'єднання, з'єднане мостом між фігурами . **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "5");
$canvas->morphology(\Imagick::MORPHOLOGY_TOP_HAT, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #20 Метод "TopHat", або, точніше, "Black TopHat", повертає пікселі, які були видалені закриттям фігури, тобто пікселі, які використовувалися для заповнення дірок, зазорів та мостів . **Imagick::morphology()****

```php
<?php

$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "5");
$canvas->morphology(\Imagick::MORPHOLOGY_BOTTOM_HAT, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #21 Приклад використання методу Hit та Miss **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
// Находит все пиксели с 3 пикселями правого края
$matrix = [[1, false, false, 0]];
$kernel = \ImagickKernel::fromMatrix(
    $matrix,
    [0, 0]
);
$canvas->morphology(\Imagick::MORPHOLOGY_HIT_AND_MISS, 1, $kernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #22 Приклад використання методу Thinning **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$leftEdgeKernel = \ImagickKernel::fromMatrix([[0, 1]], [1, 0]);
$rightEdgeKernel = \ImagickKernel::fromMatrix([[1, 0]], [0, 0]);
$leftEdgeKernel->addKernel($rightEdgeKernel);

$canvas->morphology(\Imagick::MORPHOLOGY_THINNING, 3, $leftEdgeKernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #23 Приклад використання методу Thicken **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$leftEdgeKernel = \ImagickKernel::fromMatrix([[0, 1]], [1, 0]);
$rightEdgeKernel = \ImagickKernel::fromMatrix([[1, 0]], [0, 0]);
$leftEdgeKernel->addKernel($rightEdgeKernel);

$canvas->morphology(\Imagick::MORPHOLOGY_THICKEN, 3, $leftEdgeKernel);
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #24 Приклад використання методу Thick для створення опуклої оболонки **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$diamondKernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DIAMOND, "1");
$convexKernel =  \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_CONVEX_HULL, "");

// Утолщённая морфология не справляется с небольшими зазорами.
// Закрываем их близкой морфологией.
$canvas->morphology(\Imagick::MORPHOLOGY_CLOSE, 1, $diamondKernel);
$canvas->morphology(\Imagick::MORPHOLOGY_THICKEN, -1, $convexKernel);
$canvas->morphology(\Imagick::MORPHOLOGY_CLOSE, 1, $diamondKernel);

header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #25 Приклад використання методу Iterative morphology **Imagick::morphology()****

```php
<?php
$canvas = $this->getCharacterOutline();
$kernel = \ImagickKernel::fromBuiltIn(\Imagick::KERNEL_DISK, "2");
$canvas->morphology(\Imagick::MORPHOLOGY_ITERATIVE, 3, $kernel);
$canvas->autoLevelImage();
header("Content-Type: image/png");
echo $canvas->getImageBlob();

?>
```

**Приклад #26 Приклад використання допоміжної функції для отримання силуету зображення **Imagick::morphology()****

```php
<?php

function getCharacterOutline() {
    $imagick = new \Imagick(realpath("./images/character.png"));
    $character = new \Imagick();
    $character->newPseudoImage(
        $imagick->getImageWidth(),
        $imagick->getImageHeight(),
        "canvas:white"
    );
    $canvas = new \Imagick();
    $canvas->newPseudoImage(
        $imagick->getImageWidth(),
        $imagick->getImageHeight(),
        "canvas:black"
    );

    $character->compositeimage(
        $imagick,
        \Imagick::COMPOSITE_COPYOPACITY,
        0, 0
    );
    $canvas->compositeimage(
        $character,
        \Imagick::COMPOSITE_ATOP,
        0, 0
    );
    $canvas->setFormat('png');

    return $canvas;
}
?>
```
