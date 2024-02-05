---
navigation:
  - imagick.separateimagechannel.md: '« Imagick::separateImageChannel'
  - imagick.setbackgroundcolor.md: 'Imagick::setBackgroundColor »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::sepiaToneImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

**Пример #1 Пример использования**Imagick::sepiaToneImage()\*\*\*\*

```php
<?php
function sepiaToneImage($imagePath, $sepia) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->sepiaToneImage($sepia);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
