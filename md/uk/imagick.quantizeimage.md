---
navigation:
  - imagick.profileimage.md: '« Imagick::profileImage'
  - imagick.quantizeimages.md: 'Imagick::quantizeImages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::quantizeImage'
---
# Imagick::quantizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::quantizeImage — Аналізує кольори еталонного зображення

### Опис

```methodsynopsis
public Imagick::quantizeImage(    int $numberColors,    int $colorspace,    int $treedepth,    bool $dither,    bool $measureError): bool
```

### Список параметрів

`numberColors`

`colorspace`

`treedepth`

`dither`

`measureError`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::quantizeImage()****

```php
<?php
function quantizeImage($imagePath, $numberColors, $colorSpace, $treeDepth, $dither) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->quantizeImage($numberColors, $colorSpace, $treeDepth, $dither, false);
    $imagick->setImageFormat('png');
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
