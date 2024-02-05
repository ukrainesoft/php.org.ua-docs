---
navigation:
  - imagick.levelimage.md: '« Imagick::levelImage'
  - imagick.liquidrescaleimage.md: 'Imagick::liquidRescaleImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::linearStretchImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::linearStretchImage

(PECL imagick 2, PECL imagick 3)

Imagick::linearStretchImage — Розтягує яскравість зображення з насиченням.

### Опис

```methodsynopsis
public Imagick::linearStretchImage(float $blackPoint, float $whitePoint): bool
```

Розтягує з насиченням яскравість зображення.

### Список параметрів

`blackPoint`

Чорна точка зображення

`whitePoint`

Біла точка зображення

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::linearStretchImage()\*\*\*\*

```php
<?php
function linearStretchImage($imagePath, $blackThreshold, $whiteThreshold) {
    $imagick = new \Imagick(realpath($imagePath));
    $pixels = $imagick->getImageWidth() * $imagick->getImageHeight();
    $imagick->linearStretchImage($blackThreshold * $pixels, $whiteThreshold * $pixels);

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
