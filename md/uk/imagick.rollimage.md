---
navigation:
  - imagick.resizeimage.md: '« Imagick::resizeImage'
  - imagick.rotateimage.md: 'Imagick::rotateImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::rollImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::rollImage

(PECL imagick 2, PECL imagick 3)

Imagick::rollImage — Зміщує зображення

### Опис

```methodsynopsis
public Imagick::rollImage(int $x, int $y): bool
```

Зміщує зображення відповідно до визначення x та y.

### Список параметрів

`x`

Зміщення осі X.

`y`

Зміщення осі Y.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::rollImage()\*\*\*\*

```php
<?php
function rollImage($imagePath, $rollX, $rollY) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->rollimage($rollX, $rollY);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
