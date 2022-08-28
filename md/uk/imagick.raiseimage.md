Створює імітацію ефекту 3D-кнопки

-   [« Imagick::radialBlurImage](imagick.radialblurimage.html)
    
-   [Imagick::randomThresholdImage »](imagick.randomthresholdimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Створює імітацію ефекту 3D-кнопки
    

# Imagick::raiseImage

(PECL imagick 2, PECL imagick 3)

Imagick::raiseImage — Створює імітацію ефекту 3D-кнопки

### Опис

```methodsynopsis
public Imagick::raiseImage(    int $width,    int $height,    int $x,    int $y,    bool $raise): bool
```

Створює імітацію тривимірного ефекту кнопки, освітлюючи та затемнюючи краї зображення. Ширина та висота елементів raiseinfo визначають ширину вертикального та горизонтального краю ефекту.

### Список параметрів

`width`

`height`

`x`

`y`

`raise`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::raiseImage()****

```php
<?php
function raiseImage($imagePath, $width, $height, $x, $y, $raise) {
    $imagick = new \Imagick(realpath($imagePath));

    //x и y ничего не делают?
    $imagick->raiseImage($width, $height, $x, $y, $raise);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```