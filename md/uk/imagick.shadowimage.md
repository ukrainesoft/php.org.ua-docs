Імітує тінь зображення

-   [« Imagick::shadeImage](imagick.shadeimage.html)
    
-   [Imagick::sharpenImage »](imagick.sharpenimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Імітує тінь зображення
    

# Imagick::shadowImage

(PECL imagick 2, PECL imagick 3)

Imagick::shadowImage — Імітує тінь зображення

### Опис

```methodsynopsis
public Imagick::shadowImage(    float $opacity,    float $sigma,    int $x,    int $y): bool
```

Імітує тінь зображення.

### Список параметрів

`opacity`

`sigma`

`x`

`y`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::shadowImage()****

```php
<?php
function shadowImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->shadowImage(0.4, 10, 50, 5);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```