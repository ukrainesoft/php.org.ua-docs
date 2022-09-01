---
navigation:
  - imagick.sparsecolorimage.md: '« Imagick::sparseColorImage'
  - imagick.spreadimage.md: 'Imagick::spreadImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::spliceImage'
---
# Imagick::spliceImage

(PECL imagick 2, PECL imagick 3)

Imagick::spliceImage — Склеює суцільний колір у зображення

### Опис

```methodsynopsis
public Imagick::spliceImage(    int $width,    int $height,    int $x,    int $y): bool
```

Склеює суцільний колір зображення.

### Список параметрів

`width`

`height`

`x`

`y`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::spliceImage()****

```php
<?php
function spliceImage($imagePath, $startX, $startY, $width, $height) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->spliceImage($width, $height, $startX, $startY);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
