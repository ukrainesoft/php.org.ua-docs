Застосовує обертальне розмиття до зображення

-   [« Imagick::rotateImage](imagick.rotateimage.md)
    
-   [Imagick::roundCorners »](imagick.roundcorners.md)
    
-   [PHP Manual](index.md)
    
-   [Imagick](class.imagick.md)
    
-   Застосовує обертальне розмиття до зображення
    

# Imagick::rotationalBlurImage

(PECL imagick 3> = 3.3.0)

Imagick::rotationalBlurImage — Застосовує обертальне розмиття до зображення

### Опис

```methodsynopsis
public Imagick::rotationalBlurImage(float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Застосовує обертальне розмиття зображення.

### Список параметрів

`angle`

Кут розмиття.

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::rotationalBlurImage()****

```php
<?php
function rotationalBlurImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->rotationalBlurImage(3);
    $imagick->rotationalBlurImage(5);
    $imagick->rotationalBlurImage(7);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```