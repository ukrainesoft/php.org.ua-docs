Опис

-   [« Imagick::flopImage](imagick.flopimage.md)
    
-   [Imagick::frameImage »](imagick.frameimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Опис
    

# Imagick::forwardFourierTransformImage

(PECL imagick 3> = 3.3.0)

Imagick::forwardFourierTransformImage — Опис

### Опис

```methodsynopsis
public Imagick::forwardFourierTransformimage(bool $magnitude): bool
```

Реалізує дискретне перетворення Фур'є (ДПФ) зображення у вигляді пари величина/фаза або пари, що складається з реального/уявного зображень.

### Список параметрів

`magnitude`

Якщо значення дорівнює true, буде повернуто пару величина/фаза, інакше – пара, що складається з реального/уявного зображень.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::forwardFourierTransformImage()****

```php
<?php
//Служебная функция для forwardTransformImage
function createMask() {
    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(0);
    $draw->setStrokeColor('rgb(255, 255, 255)');
    $draw->setFillColor('rgb(255, 255, 255)');

    //Рисование круга на оси Y с центром в точках
    //x, y, который касается начала координат
    $draw->circle(250, 250, 220, 250);

    $imagick = new \Imagick();
    $imagick->newImage(512, 512, "black");
    $imagick->drawImage($draw);
    $imagick->gaussianBlurImage(20, 20);
    $imagick->autoLevelImage();

    return $imagick;
}


function forwardFourierTransformImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->resizeimage(512, 512, \Imagick::FILTER_LANCZOS, 1);

    $mask = createMask();
    $imagick->forwardFourierTransformImage(true);

    @$imagick->setimageindex(0);
    $magnitude = $imagick->getimage();

    @$imagick->setimageindex(1);
    $imagickPhase = $imagick->getimage();

    if (true) {
        $imagickPhase->compositeImage($mask, \Imagick::COMPOSITE_MULTIPLY, 0, 0);
    }

    if (false) {
        $output = clone $imagickPhase;
        $output->setimageformat('png');
        header("Content-Type: image/png");
        echo $output->getImageBlob();
    }

    $magnitude->inverseFourierTransformImage($imagickPhase, true);

    $magnitude->setimageformat('png');
    header("Content-Type: image/png");
    echo $magnitude->getImageBlob();
}

?>
```