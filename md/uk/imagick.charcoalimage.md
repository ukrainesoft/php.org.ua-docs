---
navigation:
  - imagick.brightnesscontrastimage.md: '« Imagick::brightnessContrastImage'
  - imagick.chopimage.md: 'Imagick::chopImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::charcoalImage'
---
# Imagick::charcoalImage

(PECL imagick 2, PECL imagick 3)

Imagick::charcoalImage — Малювання вугіллям

### Опис

```methodsynopsis
public Imagick::charcoalImage(float $radius, float $sigma): bool
```

Малювання вугіллям.

### Список параметрів

`radius`

Радіус Гауса, у пікселях, не включаючи центральний піксель

`sigma`

Стандартне відхилення Гауса, у пікселях

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::charcoalImage()****

```php
<?php
function charcoalImage($imagePath, $radius, $sigma) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->charcoalImage($radius, $sigma);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
