---
navigation:
  - imagick.floodfillpaintimage.md: '« Imagick::floodFillPaintImage'
  - imagick.forwardfouriertransformimage.md: 'Imagick::forwardFourierTransformImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::flopImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::flopImage

(PECL imagick 2, PECL imagick 3)

Imagick::flopImage — Створює дзеркальне горизонтальне відображення.

### Опис

```methodsynopsis
public Imagick::flopImage(): bool
```

Створює горизонтальне дзеркало зображення, що відображає пікселі навколо центральної осі Y.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::flopImage()\*\*\*\*

```php
<?php
function flopImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->flopImage();
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```

### Дивіться також

-   [Imagick::flipimage()](imagick.flipimage.md) \- Створює вертикальне дзеркало зображення
