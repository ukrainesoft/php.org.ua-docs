---
navigation:
  - imagick.trimimage.md: '« Imagick::trimImage'
  - imagick.unsharpmaskimage.md: 'Imagick::unsharpMaskImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::uniqueImageColors'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::uniqueImageColors

(PECL imagick 2,PECL imagick 3)

Imagick::uniqueImageColors - Відкидає все, крім одного, будь-якого кольору пікселя

### Опис

```methodsynopsis
public Imagick::uniqueImageColors(): bool
```

Відкидає все, окрім одного, будь-якого кольору пікселя. Цей метод доступний, якщо Imagick був скомпільований із версією ImageMagick 6.2.9 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::uniqueImageColors()\*\*\*\*

```php
<?php
function uniqueImageColors($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    //Reduce the image to 256 colours nicely.
    $imagick->quantizeImage(256, \Imagick::COLORSPACE_YIQ, 0, false, false);
    $imagick->uniqueImageColors();
    $imagick->scaleimage($imagick->getImageWidth(), $imagick->getImageHeight() * 20);
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
