---
navigation:
  - imagick.swirlimage.md: '« Imagick::swirlImage'
  - imagick.thresholdimage.md: 'Imagick::thresholdImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::textureImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::textureImage

(PECL imagick 2, PECL imagick 3)

Imagick::textureImage — Багаторазово розміщує зображення текстури

### Опис

```methodsynopsis
Imagick::textureImage(Imagick $texture_wand): Imagick
```

Багаторазово розміщує зображення текстури упоперек і вниз по полотну зображення.

### Список параметрів

`texture_wand`

Об'єкт Imagick для використання як зображення текстури.

### Значення, що повертаються

Повертає новий об'єкт Imagick, до якого застосована текстура, що повторюється.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::textureImage()\*\*\*\*

```php
<?php
function textureImage($imagePath) {
    $image = new \Imagick();
    $image->newImage(640, 480, new \ImagickPixel('pink'));
    $image->setImageFormat("jpg");
    $texture = new \Imagick(realpath($imagePath));
    $texture->scaleimage($image->getimagewidth() / 4, $image->getimageheight() / 4);
    $image = $image->textureImage($texture);
    header("Content-Type: image/jpg");
    echo $image;
}

?>
```
