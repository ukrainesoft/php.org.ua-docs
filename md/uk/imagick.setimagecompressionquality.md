Встановлює якість стиснення зображення

-   [« Imagick::setImageCompression](imagick.setimagecompression.html)
    
-   [Imagick::setImageDelay »](imagick.setimagedelay.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює якість стиснення зображення
    

# Imagick::setImageCompressionQuality

(PECL imagick 2, PECL imagick 3)

Imagick::setImageCompressionQuality — Встановлює якість стиснення зображення

### Опис

```methodsynopsis
public Imagick::setImageCompressionQuality(int $quality): bool
```

Встановлює якість стиснення зображення.

### Список параметрів

`quality`

Якість стиснення зображення у вигляді цілого числа

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageCompressionQuality()****

```php
<?php
function setImageCompressionQuality($imagePath, $quality) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageCompressionQuality($quality);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```