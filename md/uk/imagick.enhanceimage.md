---
navigation:
  - imagick.encipherimage.md: '« Imagick::encipherImage'
  - imagick.equalizeimage.md: 'Imagick::equalizeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::enhanceImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::enhanceImage

(PECL imagick 2, PECL imagick 3)

Imagick::enhanceImage — Покращує якість шумного зображення

### Опис

```methodsynopsis
public Imagick::enhanceImage(): bool
```

Застосовує цифровий фільтр, що покращує якість зображення з шумом.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::enhanceImage()\*\*\*\*

```php
<?php
function enhanceImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->enhanceImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
