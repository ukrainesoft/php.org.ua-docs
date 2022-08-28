Підсилює краї зображення

-   [« Imagick::drawImage](imagick.drawimage.html)
    
-   [Imagick::embossImage »](imagick.embossimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Підсилює краї зображення
    

# Imagick::edgeImage

(PECL imagick 2, PECL imagick 3)

Imagick::edgeImage — Підсилює краї зображення.

### Опис

```methodsynopsis
public Imagick::edgeImage(float $radius): bool
```

Збільшує краї зображення за допомогою фільтра згортки даного радіуса. Використовуйте радіус 0, і його буде обрано автоматично.

### Список параметрів

`radius`

Радіус операції.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::edgeImage()****

```php
<?php
function edgeImage($imagePath, $radius) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->edgeImage($radius);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```