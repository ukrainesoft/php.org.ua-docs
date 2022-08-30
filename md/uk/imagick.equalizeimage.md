Вирівнює гістограму зображення

-   [« Imagick::enhanceImage](imagick.enhanceimage.md)
    
-   [Imagick::evaluateImage »](imagick.evaluateimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Вирівнює гістограму зображення
    

# Imagick::equalizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::equalizeImage — Вирівнює гістограму зображення

### Опис

```methodsynopsis
public Imagick::equalizeImage(): bool
```

Вирівнює гістограму зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::equalizeImage()****

```php
<?php
function equalizeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->equalizeImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```