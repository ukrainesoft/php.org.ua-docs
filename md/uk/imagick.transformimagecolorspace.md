Перетворює зображення на новий колірний простір

-   [« Imagick::transformImage](imagick.transformimage.html)
    
-   [Imagick::transparentPaintImage »](imagick.transparentpaintimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Перетворює зображення на новий колірний простір
    

# Imagick::transformImageColorspace

(PECL imagick 3)

Imagick::transformImageColorspace — Перетворення зображення на новий колірний простір

### Опис

```methodsynopsis
public Imagick::transformImageColorspace(int $colorspace): bool
```

Перетворює зображення на новий колірний простір.

### Список параметрів

`colorspace`

Колірний простір, в який має бути перетворено зображення, одна з[констант COLORSPACE](imagick.constants.html#imagick.constants.colorspace)наприклад Imagick::COLORSPACECMYK.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::transformImageColorspace()****

Перетворює зображення на новий колірний простір, а потім витягує окремий канал, щоб можна було переглянути значення окремих каналів.

```php
<?php
function transformImageColorspace($imagePath, $colorSpace, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->transformimagecolorspace($colorSpace);
    //канал должен быть одной из констант канала, например \Imagick::CHANNEL_BLUE
    $imagick->separateImageChannel($channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}
?>
```

### Дивіться також

-   [Imagick::setColorSpace()](imagick.setcolorspace.html) - Встановлює колірний простір