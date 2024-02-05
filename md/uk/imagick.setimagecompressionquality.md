---
navigation:
  - imagick.setimagecompression.md: '« Imagick::setImageCompression'
  - imagick.setimagedelay.md: 'Imagick::setImageDelay »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageCompressionQuality'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageCompressionQuality

(PECL imagick 2, PECL imagick 3)

Imagick::setImageCompressionQuality — Встановлює якість стиснення зображення

### Опис

```methodsynopsis
public Imagick::setImageCompressionQuality(int $quality): bool
```

Встановлює якість стиснення зображення.

### Список параметрів

`quality`

Якість стиснення зображення у вигляді цілого числа

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::setImageCompressionQuality()\*\*\*\*

```php
<?php
function setImageCompressionQuality($imagePath, $quality) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageCompressionQuality($quality);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
