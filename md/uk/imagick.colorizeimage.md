---
navigation:
  - imagick.colorfloodfillimage.md: '« Imagick::colorFloodfillImage'
  - imagick.colormatriximage.md: 'Imagick::colorMatrixImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::colorizeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::colorizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::colorizeImage — Змішування кольору заливки із зображенням

### Опис

```methodsynopsis
public Imagick::colorizeImage(mixed $colorize, mixed $opacity, bool $legacy = false): bool
```

Змішує колір заливки з кожним пікселем зображення.

### Список параметрів

`colorize`

Об'єкт ImagickPixel або рядок, що містить колір

`opacity`

Об'єкт ImagickPixel або дробове число, що містить прозорість. 1.0 означає без прозорості; 0.0 означає повну прозорість.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Для першого параметра можна передавати колір у вигляді рядка та вказувати значення прозорості у другому параметрі. Попередні версії допускали лише об'єкт ImagickPixel. |

### Приклади

**Пример #1 Пример использования**Imagick::colorizeImage()\*\*\*\*

```php
<?php
function colorizeImage($imagePath, $color, $opacity) {
    $imagick = new \Imagick(realpath($imagePath));
    $opacity = $opacity / 255.0;
    $opacityColor = new \ImagickPixel("rgba(0, 0, 0, $opacity)");
    $imagick->colorizeImage($color, $opacityColor);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
