Випадково зміщує кожен піксель у блоці

-   [« Imagick::spliceImage](imagick.spliceimage.html)
    
-   [Imagick::statisticImage »](imagick.statisticimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Випадково зміщує кожен піксель у блоці
    

# Imagick::spreadImage

(PECL imagick 2, PECL imagick 3)

Imagick::spreadImage — Випадково зміщує кожен піксель у блоці

### Опис

```methodsynopsis
public Imagick::spreadImage(float $radius): bool
```

Метод спеціальних ефектів, який випадково зміщує кожен піксель у блоці, заданому параметром radius.

### Список параметрів

`radius`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::spreadImage()****

```php
<?php
function spreadImage($imagePath, $radius) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->spreadImage($radius);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```