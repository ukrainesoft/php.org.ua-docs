---
navigation:
  - imagick.identifyimage.md: '« Imagick::identifyImage'
  - imagick.importimagepixels.md: 'Imagick::importImagePixels »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::implodeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::implodeImage

(PECL imagick 2, PECL imagick 3)

Imagick::implodeImage — Створює копію зображення

### Опис

```methodsynopsis
public Imagick::implodeImage(float $radius): bool
```

Створює нове зображення, яке є копією існуючого з пікселями, "стиснутими" на зазначений відсоток.

### Список параметрів

`radius`

Радіус стиснення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::implodeImage()\*\*\*\*

```php
<?php
function implodeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->implodeImage(0.0001);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();

}

?>
```
