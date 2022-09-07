---
navigation:
  - imagick.shadeimage.md: '« Imagick::shadeImage'
  - imagick.sharpenimage.md: 'Imagick::sharpenImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::shadowImage'
---
# Imagick::shadowImage

(PECL imagick 2, PECL imagick 3)

Imagick::shadowImage — Імітує тінь зображення

### Опис

```methodsynopsis
public Imagick::shadowImage(    float $opacity,    float $sigma,    int $x,    int $y): bool
```

Імітує тінь зображення.

### Список параметрів

`opacity`

`sigma`

`x`

`y`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::shadowImage()****

```php
<?php
function shadowImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->shadowImage(0.4, 10, 50, 5);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
