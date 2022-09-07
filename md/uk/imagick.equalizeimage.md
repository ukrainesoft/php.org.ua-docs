---
navigation:
  - imagick.enhanceimage.md: '« Imagick::enhanceImage'
  - imagick.evaluateimage.md: 'Imagick::evaluateImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::equalizeImage'
---
# Imagick::equalizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::equalizeImage — Вирівнює гістограму зображення

### Опис

```methodsynopsis
public Imagick::equalizeImage(): bool
```

Вирівнює гістограму зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::equalizeImage()****

```php
<?php
function equalizeImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->equalizeImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
