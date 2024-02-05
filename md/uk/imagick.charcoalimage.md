---
navigation:
  - imagick.brightnesscontrastimage.md: '« Imagick::brightnessContrastImage'
  - imagick.chopimage.md: 'Imagick::chopImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::charcoalImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**Imagick::charcoalImage()\*\*\*\*

```php
<?php
function charcoalImage($imagePath, $radius, $sigma) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->charcoalImage($radius, $sigma);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
