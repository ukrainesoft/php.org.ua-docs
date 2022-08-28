Створює горизонтальне дзеркальне відображення

-   [« Imagick::floodFillPaintImage](imagick.floodfillpaintimage.html)
    
-   [Imagick::forwardFourierTransformImage »](imagick.forwardfouriertransformimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює горизонтальне дзеркальне відображення
    

# Imagick::flopImage

(PECL imagick 2, PECL imagick 3)

Imagick::flopImage — Створює дзеркальне горизонтальне відображення.

### Опис

```methodsynopsis
public Imagick::flopImage(): bool
```

Створює горизонтальне дзеркало зображення, що відображає пікселі навколо центральної осі Y.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::flopImage()****

```php
<?php
function flopImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->flopImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::flipimage()](imagick.flipimage.html) - Створює вертикальне дзеркало зображення