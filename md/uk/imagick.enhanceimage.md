Покращує якість шумного зображення

-   [« Imagick::encipherImage](imagick.encipherimage.html)
    
-   [Imagick::equalizeImage »](imagick.equalizeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Покращує якість шумного зображення
    

# Imagick::enhanceImage

(PECL imagick 2, PECL imagick 3)

Imagick::enhanceImage — Покращує якість шумного зображення

### Опис

```methodsynopsis
public Imagick::enhanceImage(): bool
```

Застосовує цифровий фільтр, що покращує якість зображення з шумом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::enhanceImage()****

```php
<?php
function enhanceImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->enhanceImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```