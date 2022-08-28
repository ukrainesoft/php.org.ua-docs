Опис

-   [« Imagick::spreadImage](imagick.spreadimage.html)
    
-   [Imagick::steganoImage »](imagick.steganoimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Опис
    

# Imagick::statisticImage

(PECL imagick 3> = 3.3.0)

Imagick::statisticImage — Опис

### Опис

```methodsynopsis
public Imagick::statisticImage(    int $type,    int $width,    int $height,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Замінює кожен піксель відповідною статистикою з околиці зазначеної ширини та висоти.

### Список параметрів

`type`

`width`

`height`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::statisticImage()****

```php
<?php
function statisticImage($imagePath, $statisticType, $width, $height, $channel) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->statisticImage(
        $statisticType,
        $width,
        $height,
        $channel
    );

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

statisticImage($imagePath, \Imagick::STATISTIC_MEDIAN, 5, 5, \Imagick::CHANNEL_DEFAULT);

?>
```