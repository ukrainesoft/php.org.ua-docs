---
navigation:
  - imagick.subimagematch.html: '« Imagick::subImageMatch'
  - imagick.textureimage.html: 'Imagick::textureImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::swirlImage'
---
# Imagick::swirlImage

(PECL imagick 2, PECL imagick 3)

Imagick::swirlImage — Закручує пікселі навколо центру зображення

### Опис

```methodsynopsis
Imagick::swirlImage(float $degrees): bool
```

Закручує пікселі навколо центру зображення, де градуси вказують розмах дуги, якою переміщається кожен піксель. Ви отримуєте драматичніший ефект, коли градуси переміщуються від 1 до 360.

### Список параметрів

`degrees`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::swirlImage()****

```php
<?php
function swirlImage($imagePath, $swirl) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->swirlImage($swirl);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
