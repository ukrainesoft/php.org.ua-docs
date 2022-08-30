Накладає випадковий шум на зображення

-   [« Imagick::addImage](imagick.addimage.html)
    
-   [Imagick::affineTransformImage »](imagick.affinetransformimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Накладає випадковий шум на зображення
    

# Imagick::addNoiseImage

(PECL imagick 2, PECL imagick 3)

Imagick::addNoiseImage — Накладає випадковий шум на зображення

### Опис

```methodsynopsis
public Imagick::addNoiseImage(int $noise_type, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Накладає випадковий шум зображення.

### Список параметрів

`noise_type`

Тип шуму. Зверніться до списку [констант шума](imagick.constants.html#imagick.constants.noise)

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константы каналов](imagick.constants.html#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.html#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::addNoiseImage()****

```php
<?php
function addNoiseImage($noiseType, $imagePath, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->addNoiseImage($noiseType, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```