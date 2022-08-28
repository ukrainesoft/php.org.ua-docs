Радіальне розмиття зображення

-   [« Imagick::queryFormats](imagick.queryformats.html)
    
-   [Imagick::raiseImage »](imagick.raiseimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Радіальне розмиття зображення
    

# Imagick::radialBlurImage

(PECL imagick 2, PECL imagick 3)

Imagick::radialBlurImage — Радіальне розмиття зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::radialBlurImage(float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Радіальне розмиття зображення.

### Список параметрів

`angle`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::radialBlurImage()****

```php
<?php
function radialBlurImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    //Размытие 3 раза с разными радиусами
    $imagick->radialBlurImage(3);
    $imagick->radialBlurImage(5);
    $imagick->radialBlurImage(7);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```