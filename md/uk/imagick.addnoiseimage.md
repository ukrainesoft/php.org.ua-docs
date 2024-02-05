---
navigation:
  - imagick.addimage.md: '« Imagick::addImage'
  - imagick.affinetransformimage.md: 'Imagick::affineTransformImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::addNoiseImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Тип шума. Обратитесь к списку[констант шуму](imagick.constants.md#imagick.constants.noise)

`channel`

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно \*\*`Imagick::CHANNEL_DEFAULT`\*\*Обратитесь к списку[констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::addNoiseImage()\*\*\*\*

```php
<?php
function addNoiseImage($noiseType, $imagePath, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->addNoiseImage($noiseType, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
