Створює копію зображення

-   [« Imagick::identifyImage](imagick.identifyimage.html)
    
-   [Imagick::importImagePixels »](imagick.importimagepixels.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює копію зображення
    

# Imagick::implodeImage

(PECL imagick 2, PECL imagick 3)

Imagick::implodeImage — Створює копію зображення

### Опис

```methodsynopsis
public Imagick::implodeImage(float $radius): bool
```

Створює нове зображення, яке є копією існуючого з пікселями, "стиснутими" на зазначений відсоток.

### Список параметрів

`radius`

Радіус стиснення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::implodeImage()****

```php
<?php
function implodeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->implodeImage(0.0001);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();

}

?>
```