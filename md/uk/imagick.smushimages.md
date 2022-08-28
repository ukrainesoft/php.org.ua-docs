Опис

-   [« Imagick::sketchImage](imagick.sketchimage.html)
    
-   [Imagick::solarizeImage »](imagick.solarizeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Опис
    

# Imagick::smushImages

(PECL imagick 3> = 3.3.0)

Imagick::smushImages — Опис

### Опис

```methodsynopsis
public Imagick::smushImages(bool $stack, int $offset): Imagick
```

Бере всі зображення з поточного покажчика зображення в кінець списку зображень і переміщує їх одне до одного зверху вниз, якщо параметр stack має значення true, інакше - зліва направо.

### Список параметрів

`stack`

`offset`

### Значення, що повертаються

Нове розмите зображення.

### Приклади

**Приклад #1 Приклад використання **Imagick::smushImages()****

```php
<?php
function smushImages($imagePath, $imagePath2) {

    $imagick = new \Imagick(realpath($imagePath));
    $imagick2 = new \Imagick(realpath($imagePath2));

    $imagick->addimage($imagick2);
    $smushed = $imagick->smushImages(false, 50);
    $smushed->setImageFormat('jpg');
    header("Content-Type: image/jpg");
    echo $smushed->getImageBlob();
}

?>
```