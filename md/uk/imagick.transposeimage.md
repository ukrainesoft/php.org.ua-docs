Створює вертикальне дзеркальне відображення

-   [« Imagick::transparentPaintImage](imagick.transparentpaintimage.html)
    
-   [Imagick::transverseImage »](imagick.transverseimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює вертикальне дзеркальне відображення
    

# Imagick::transposeImage

(PECL imagick 2, PECL imagick 3)

Imagick::transposeImage — Створює вертикальне дзеркальне відображення

### Опис

```methodsynopsis
public Imagick::transposeImage(): bool
```

Створює вертикальне дзеркальне зображення, відбиваючи пікселі навколо центральної осі X, повертаючи їх у 90 градусів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::transposeImage()****

```php
<?php
function transposeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->transposeImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::transverseImage()](imagick.transverseimage.html) - Створює горизонтальне дзеркальне відображення