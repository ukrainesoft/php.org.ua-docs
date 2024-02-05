---
navigation:
  - imagick.rotateimage.md: '« Imagick::rotateImage'
  - imagick.roundcorners.md: 'Imagick::roundCorners »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::rotationalBlurImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::rotationalBlurImage

(PECL imagick 3 >= 3.3.0)

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

Передайте будь-яку коректну для вашого режиму каналу константу. Для застосування до більш ніж одного каналу комбінуйте [константи каналів](imagick.constants.md#imagick.constants.channel) за допомогою побітових операторів. За замовчуванням одно \*\*`Imagick::CHANNEL_DEFAULT`\*\*Обратитесь к списку[констант каналів](imagick.constants.md#imagick.constants.channel)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::rotationalBlurImage()\*\*\*\*

```php
<?php
function rotationalBlurImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->rotationalBlurImage(3);
    $imagick->rotationalBlurImage(5);
    $imagick->rotationalBlurImage(7);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
