---
navigation:
  - imagick.polaroidimage.md: '« Imagick::polaroidImage'
  - imagick.previewimages.md: 'Imagick::previewImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::posterizeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::posterizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::posterizeImage — Зменшує зображення до обмеженої кількості рівнів кольору

### Опис

```methodsynopsis
public Imagick::posterizeImage(int $levels, bool $dither): bool
```

Зменшує зображення до обмеженої кількості рівнів кольору.

### Список параметрів

`levels`

`dither`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::posterizeImage()\*\*\*\*

```php
<?php
function posterizeImage($imagePath, $posterizeType, $numberLevels) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->posterizeImage($numberLevels, $posterizeType);
    $imagick->setImageFormat('png');
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

posterizeImage($imagePath, \Imagick::DITHERMETHOD_RIEMERSMA, 8);

?>
```
