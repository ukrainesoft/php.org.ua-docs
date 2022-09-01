---
navigation:
  - imagick.separateimagechannel.html: '« Imagick::separateImageChannel'
  - imagick.setbackgroundcolor.html: 'Imagick::setBackgroundColor »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::sepiaToneImage'
---
# Imagick::sepiaToneImage

(PECL imagick 2, PECL imagick 3)

Imagick::sepiaToneImage — Тонування зображення сепією

### Опис

```methodsynopsis
public Imagick::sepiaToneImage(float $threshold): bool
```

Застосовує до зображення спеціальний ефект, аналогічний ефекту, що досягається фотолабораторії за допомогою тонування сепією. Поріг варіюється від 0 до QuantumRange і є мірою тонування сепії. Поріг 80 - відправна точка для розумного тону.

### Список параметрів

`threshold`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::sepiaToneImage()****

```php
<?php
function sepiaToneImage($imagePath, $sepia) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->sepiaToneImage($sepia);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
