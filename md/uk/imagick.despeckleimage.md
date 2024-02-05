---
navigation:
  - imagick.deskewimage.md: '« Imagick::deskewImage'
  - imagick.destroy.md: 'Imagick::destroy »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::despeckleImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::despeckleImage

(PECL imagick 2, PECL imagick 3)

Imagick::despeckleImage — Зменшує шум на зображенні.

### Опис

```methodsynopsis
public Imagick::despeckleImage(): bool
```

Зменшує шум на зображенні, зберігаючи краї вихідного зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::despeckleImage()\*\*\*\*

```php
<?php
function despeckleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->despeckleImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
