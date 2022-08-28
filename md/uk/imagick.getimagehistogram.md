Повертає гістограму зображення

-   [« Imagick::getImageHeight](imagick.getimageheight.html)
    
-   [Imagick::getImageIndex »](imagick.getimageindex.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Повертає гістограму зображення
    

# Imagick::getImageHistogram

(PECL imagick 2, PECL imagick 3)

Imagick::getImageHistogram — Повертає гістограму зображення

### Опис

```methodsynopsis
public Imagick::getImageHistogram(): array
```

Повертає гістограму зображення у вигляді масиву об'єктів ImagickPixel.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає гістограму зображення у вигляді масиву об'єктів ImagickPixel.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Генерація **Imagick::getImageHistogram()****

```php
<?php
function getColorStatistics($histogramElements, $colorChannel) {
    $colorStatistics = [];

    foreach ($histogramElements as $histogramElement) {
        $color = $histogramElement->getColorValue($colorChannel);
        $color = intval($color * 255);
        $count = $histogramElement->getColorCount();

        if (array_key_exists($color, $colorStatistics)) {
            $colorStatistics[$color] += $count;
        }
        else {
            $colorStatistics[$color] = $count;
        }
    }

    ksort($colorStatistics);

    return $colorStatistics;
}



function getImageHistogram($imagePath) {

    $backgroundColor = 'black';

    $draw = new \ImagickDraw();
    $draw->setStrokeWidth(0); // делает линии маскимально тонкими

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    $histogramWidth = 256;
    $histogramHeight = 100; // высота для каждого сегмента RGB

    $imagick = new \Imagick(realpath($imagePath));
    //Измените размер изображения, чтобы он был маленьким, иначе PHP может не хватить памяти
    //Это может привести к плохим результатам для изображений, которые являются патологически "пиксельными"
    $imagick->adaptiveResizeImage(200, 200, true);
    $histogramElements = $imagick->getImageHistogram();

    $histogram = new \Imagick();
    $histogram->newpseudoimage($histogramWidth, $histogramHeight * 3, 'xc:black');
    $histogram->setImageFormat('png');

    $getMax = function ($carry, $item)  {
        if ($item > $carry) {
            return $item;
        }
        return $carry;
    };

    $colorValues = [
        'red' => getColorStatistics($histogramElements, \Imagick::COLOR_RED),
        'lime' => getColorStatistics($histogramElements, \Imagick::COLOR_GREEN),
        'blue' => getColorStatistics($histogramElements, \Imagick::COLOR_BLUE),
    ];

    $max = array_reduce($colorValues['red'] , $getMax, 0);
    $max = array_reduce($colorValues['lime'] , $getMax, $max);
    $max = array_reduce($colorValues['blue'] , $getMax, $max);

    $scale =  $histogramHeight / $max;

    $count = 0;
    foreach ($colorValues as $color => $values) {
        $draw->setstrokecolor($color);

        $offset = ($count + 1) * $histogramHeight;

        foreach ($values as $index => $value) {
            $draw->line($index, $offset, $index, $offset - ($value * $scale));
        }
        $count++;
    }

    $histogram->drawImage($draw);

    header( "Content-Type: image/png" );
    echo $histogram;
}

?>
```