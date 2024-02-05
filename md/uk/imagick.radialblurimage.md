---
navigation:
  - imagick.queryformats.md: '« Imagick::queryFormats'
  - imagick.raiseimage.md: 'Imagick::raiseImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::radialBlurImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::radialBlurImage

(PECL imagick 2, PECL imagick 3)

Imagick::radialBlurImage — Радіальне розмиття зображення

**Увага**

Функція оголошена *застарілої* в Imagick 3.4.4. Покладатися на цю функцію не рекомендується.

### Опис

```methodsynopsis
public Imagick::radialBlurImage(float $angle, int $channel = Imagick::CHANNEL_DEFAULT): bool
```

Радіальне розмиття зображення.

### Список параметрів

`angle`

`channel`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::radialBlurImage()\*\*\*\*

```php
<?php
function radialBlurImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    //Размытие 3 раза с разными радиусами
    $imagick->radialBlurImage(3);
    $imagick->radialBlurImage(5);
    $imagick->radialBlurImage(7);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
