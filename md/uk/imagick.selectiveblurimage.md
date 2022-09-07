---
navigation:
  - imagick.segmentimage.md: '« Imagick::segmentImage'
  - imagick.separateimagechannel.md: 'Imagick::separateImageChannel »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::selectiveBlurImage'
---
# Imagick::selectiveBlurImage

(PECL imagick 3> = 3.3.0)

Imagick::selectiveBlurImage — Опис

### Опис

```methodsynopsis
public Imagick::selectiveBlurImage(    float $radius,    float $sigma,    float $threshold,    int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Вибіркове розмиття зображення у межах порогового значення контрастності. Це схоже на маску нерізкості, яка збільшує різкість всього, якщо контраст перевищує певний поріг.

### Список параметрів

`radius`

`sigma`

`threshold`

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно **`Imagick::CHANNEL_DEFAULT`**. Зверніться до списку [констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::selectiveBlurImage()****

```php
<?php
function selectiveBlurImage($imagePath, $radius, $sigma, $threshold, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->selectiveBlurImage($radius, $sigma, $threshold, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
