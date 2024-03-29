---
navigation:
  - imagick.transformimage.md: '« Imagick::transformImage'
  - imagick.transparentpaintimage.md: 'Imagick::transparentPaintImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::transformImageColorspace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::transformImageColorspace

(PECL imagick 3)

Imagick::transformImageColorspace — Перетворює зображення на новий колірний простір.

### Опис

```methodsynopsis
public Imagick::transformImageColorspace(int $colorspace): bool
```

Перетворює зображення на новий колірний простір.

### Список параметрів

`colorspace`

Колірний простір, в який має бути перетворено зображення, одна з[констант COLORSPACE](imagick.constants.md#imagick.constants.colorspace)наприклад Imagick::COLORSPACE\_CMYK.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад использования метода**Imagick::transformImageColorspace()\*\*\*\*

Перетворює зображення на новий колірний простір, а потім витягує окремий канал, щоб можна було переглянути значення окремих каналів.

```php
<?php
function transformImageColorspace($imagePath, $colorSpace, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->transformimagecolorspace($colorSpace);
    //канал должен быть одной из констант канала, наПриклад \Imagick::CHANNEL_BLUE
    $imagick->separateImageChannel($channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}
?>
```

### Дивіться також

-   [Imagick::setColorSpace()](imagick.setcolorspace.md) \- Встановлює колірний простір
