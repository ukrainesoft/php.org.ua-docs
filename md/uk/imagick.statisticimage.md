---
navigation:
  - imagick.spreadimage.md: '« Imagick::spreadImage'
  - imagick.steganoimage.md: 'Imagick::steganoImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::statisticImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::statisticImage

(PECL imagick 3 >= 3.3.0)

Imagick::statisticImage — Модифікація зображення за допомогою функції статистики

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

**Приклад #1 Приклад використання** Imagick::statisticImage()\*\*\*\*

```php
<?php
function statisticImage($imagePath, $statisticType, $width, $height, $channel) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->statisticImage(
        $statisticType,
        $width,
        $height,
        $channel
    );

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

statisticImage($imagePath, \Imagick::STATISTIC_MEDIAN, 5, 5, \Imagick::CHANNEL_DEFAULT);

?>
```
