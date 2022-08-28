Розтягує з насиченням яскравість зображення

-   [« Imagick::levelImage](imagick.levelimage.html)
    
-   [Imagick::liquidRescaleImage »](imagick.liquidrescaleimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Розтягує з насиченням яскравість зображення
    

# Imagick::linearStretchImage

(PECL imagick 2, PECL imagick 3)

Imagick::linearStretchImage — Розтягує яскравість зображення з насиченням.

### Опис

```methodsynopsis
public Imagick::linearStretchImage(float $blackPoint, float $whitePoint): bool
```

Розтягує з насиченням яскравість зображення.

### Список параметрів

`blackPoint`

Чорна точка зображення

`whitePoint`

Біла точка зображення

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::linearStretchImage()****

```php
<?php
function linearStretchImage($imagePath, $blackThreshold, $whiteThreshold) {
    $imagick = new \Imagick(realpath($imagePath));
    $pixels = $imagick->getImageWidth() * $imagick->getImageHeight();
    $imagick->linearStretchImage($blackThreshold * $pixels, $whiteThreshold * $pixels);

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```