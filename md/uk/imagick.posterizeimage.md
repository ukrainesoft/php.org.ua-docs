Зменшує зображення до обмеженої кількості рівнів кольору

-   [« Imagick::polaroidImage](imagick.polaroidimage.html)
    
-   [Imagick::previewImages »](imagick.previewimages.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Зменшує зображення до обмеженої кількості рівнів кольору
    

# Imagick::posterizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::posterizeImage — Зменшує зображення до обмеженої кількості рівнів кольору

### Опис

```methodsynopsis
public Imagick::posterizeImage(int $levels, bool $dither): bool
```

Зменшує зображення до обмеженої кількості рівнів кольору.

### Список параметрів

`levels`

`dither`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::posterizeImage()****

```php
<?php
function posterizeImage($imagePath, $posterizeType, $numberLevels) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->posterizeImage($numberLevels, $posterizeType);
    $imagick->setImageFormat('png');
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

posterizeImage($imagePath, \Imagick::DITHERMETHOD_RIEMERSMA, 8);

?>
```