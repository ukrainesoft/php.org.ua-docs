Опис

-   [« Imagick::segmentImage](imagick.segmentimage.html)
    
-   [Imagick::separateImageChannel »](imagick.separateimagechannel.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Опис
    

# Imagick::selectiveBlurImage

(PECL imagick 3> = 3.3.0)

Imagick::selectiveBlurImage — Опис

### Опис

```methodsynopsis
public Imagick::selectiveBlurImage(    float $radius,    float $sigma,    float $threshold,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Вибіркове розмиття зображення у межах порогового значення контрастності. Це схоже на маску нерізкості, яка збільшує різкість всього, якщо контраст перевищує певний поріг.

### Список параметрів

`radius`

`sigma`

`threshold`

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::selectiveBlurImage()****

```php
<?php
function selectiveBlurImage($imagePath, $radius, $sigma, $threshold, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->selectiveBlurImage($radius, $sigma, $threshold, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```