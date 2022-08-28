Зменшує спекл-шум на зображенні

-   [« Imagick::deskewImage](imagick.deskewimage.html)
    
-   [Imagick::destroy »](imagick.destroy.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Зменшує спекл-шум на зображенні
    

# Imagick::despeckleImage

(PECL imagick 2, PECL imagick 3)

Imagick::despeckleImage — Зменшує шум на зображенні.

### Опис

```methodsynopsis
public Imagick::despeckleImage(): bool
```

Зменшує шум на зображенні, зберігаючи краї вихідного зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::despeckleImage()****

```php
<?php
function despeckleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->despeckleImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```