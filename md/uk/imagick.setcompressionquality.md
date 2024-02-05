---
navigation:
  - imagick.setcompression.md: '« Imagick::setCompression'
  - imagick.setfilename.md: 'Imagick::setFilename »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setCompressionQuality'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setCompressionQuality

(PECL imagick 2, PECL imagick 3)

Imagick::setCompressionQuality — Встановлює якість стандартного стиснення об'єкта.

### Опис

```methodsynopsis
public Imagick::setCompressionQuality(int $quality): bool
```

Встановлює якість стандартного стиснення об'єкта.

**Застереження**

Цей метод працює тільки для нових зображень, наприклад, створених за допомогою Imagick::newPseudoImage. Для існуючих зображень слід використовувати [Imagick::setImageCompressionQuality()](imagick.setimagecompressionquality.md)

### Список параметрів

`quality`

Ціле число (int) від 1 до 100, 1 = високий рівень стиснення, 100 = низький рівень стиснення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::setCompressionQuality()\*\*\*\*

```php
<?php
function setCompressionQuality($imagePath, $quality) {

    $backgroundImagick = new \Imagick(realpath($imagePath));
    $imagick = new \Imagick();
    $imagick->setCompressionQuality($quality);
    $imagick->newPseudoImage(
        $backgroundImagick->getImageWidth(),
        $backgroundImagick->getImageHeight(),
        'canvas:white'
    );

    $imagick->compositeImage(
        $backgroundImagick,
        \Imagick::COMPOSITE_ATOP,
        0,
        0
    );

    $imagick->setFormat("jpg");
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
