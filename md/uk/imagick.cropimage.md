---
navigation:
  - imagick.count.md: '« Imagick::count'
  - imagick.cropthumbnailimage.md: 'Imagick::cropThumbnailImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::cropImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::cropImage

(PECL imagick 2, PECL imagick 3)

Imagick::cropImage — Витягує область зображення

### Опис

```methodsynopsis
public Imagick::cropImage(    int $width,    int $height,    int $x,    int $y): bool
```

Витягує область зображення.

### Список параметрів

`width`

Ширина обрізання

`height`

Висота обрізання

`x`

Координата X верхнього лівого кута області обрізання

`y`

Координата Y верхнього лівого кута області обрізання

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::cropImage()\*\*\*\*

```php
<?php
function cropImage($imagePath, $startX, $startY, $width, $height) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->cropImage($width, $height, $startX, $startY);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
