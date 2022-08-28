Створює вертикальне дзеркало зображення

-   [« Imagick::flattenImages](imagick.flattenimages.html)
    
-   [Imagick::floodFillPaintImage »](imagick.floodfillpaintimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює вертикальне дзеркало зображення
    

# Imagick::flipImage

(PECL imagick 2, PECL imagick 3)

Imagick::flipImage — Створює вертикальне дзеркало зображення

### Опис

```methodsynopsis
public Imagick::flipImage(): bool
```

Створює вертикальне дзеркало зображення, що відображає пікселі навколо центральної осі X.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::flipImage()****

```php
<?php
function flipImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->flipImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::flopimage()](imagick.flopimage.html) - Створює горизонтальне дзеркальне відображення