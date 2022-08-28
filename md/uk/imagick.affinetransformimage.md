Перетворення зображення

-   [« Imagick::addNoiseImage](imagick.addnoiseimage.html)
    
-   [Imagick::animateImages »](imagick.animateimages.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перетворення зображення
    

# Imagick::affineTransformImage

(PECL imagick 2, PECL imagick 3)

Imagick::affineTransformImage — Перетворення зображення

### Опис

```methodsynopsis
public Imagick::affineTransformImage(ImagickDraw $matrix): bool
```

Перетворення зображення за допомогою афінної матриці.

### Список параметрів

`matrix`

Афінна матриця

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::affineTransformImage()****

```php
<?php
function affineTransformImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $draw = new \ImagickDraw();

    $angle = deg2rad(40);

    $affineRotate = array(
        "sx" => cos($angle), "sy" => cos($angle),
        "rx" => sin($angle), "ry" => -sin($angle),
        "tx" => 0, "ty" => 0,
    );

    $draw->affine($affineRotate);

    $imagick->affineTransformImage($draw);

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```