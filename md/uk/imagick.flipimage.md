---
navigation:
  - imagick.flattenimages.md: '« Imagick::flattenImages'
  - imagick.floodfillpaintimage.md: 'Imagick::floodFillPaintImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::flipImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::flipImage

(PECL imagick 2, PECL imagick 3)

Imagick::flipImage — Створює вертикальне дзеркало зображення

### Опис

```methodsynopsis
public Imagick::flipImage(): bool
```

Створює вертикальне дзеркало зображення, що відображає пікселі навколо центральної осі X.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::flipImage()\*\*\*\*

```php
<?php
function flipImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->flipImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::flopimage()](imagick.flopimage.md) \- Створює горизонтальне дзеркальне відображення
