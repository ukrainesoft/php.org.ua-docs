Перетворює зображення до бажаного дозволу

-   [« Imagick::render](imagick.render.html)
    
-   [Imagick::resetImagePage »](imagick.resetimagepage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перетворює зображення до бажаного дозволу
    

# Imagick::resampleImage

(PECL imagick 2, PECL imagick 3)

Imagick::resampleImage — Перетворює зображення до бажаного дозволу

### Опис

```methodsynopsis
public Imagick::resampleImage(    float $x_resolution,    float $y_resolution,    int $filter,    float $blur): bool
```

Перетворює зображення до бажаного дозволу.

### Список параметрів

`x_resolution`

`y_resolution`

`filter`

`blur`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::resampleImage()****

```php
<?php
function resampleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->resampleImage(200, 200, \Imagick::FILTER_LANCZOS, 1);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```