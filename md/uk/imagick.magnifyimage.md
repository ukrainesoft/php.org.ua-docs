Пропорційно масштабує зображення вдвічі

-   [« Imagick::listRegistry](imagick.listregistry.md)
    
-   [Imagick::mapImage »](imagick.mapimage.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Пропорційно масштабує зображення вдвічі
    

# Imagick::magnifyImage

(PECL imagick 2, PECL imagick 3)

Imagick::magnifyImage — Пропорційно масштабує зображення вдвічі

### Опис

```methodsynopsis
public Imagick::magnifyImage(): bool
```

Масштабує зображення вдвічі пропорційно оригінальному розміру.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::magnifyImage()****

```php
<?php
function magnifyImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->magnifyImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```