---
navigation:
  - imagick.shadowimage.md: '« Imagick::shadowImage'
  - imagick.shaveimage.md: 'Imagick::shaveImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::sharpenImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::sharpenImage

(PECL imagick 2, PECL imagick 3)

Imagick::sharpenImage — Підвищує різкість зображення

### Опис

```methodsynopsis
public Imagick::sharpenImage(float $radius, float $sigma, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Підвищує різкість зображення. Згортання зображення за допомогою гаусівського оператора заданого радіусу та стандартного відхилення (сигма). Для розумних результатів радіус має бути більшим за сигму. Використовуйте радіус 0, та **Imagick::sharpenImage()** вибере потрібний вам радіус.

### Список параметрів

`radius`

`sigma`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::sharpenImage()\*\*\*\*

```php
<?php
function sharpenImage($imagePath, $radius, $sigma, $channel) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->sharpenimage($radius, $sigma, $channel);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
