---
navigation:
  - imagick.setimageopacity.md: '« Imagick::setImageOpacity'
  - imagick.setimagepage.md: 'Imagick::setImagePage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageOrientation'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageOrientation

(PECL imagick 2, PECL imagick 3)

Imagick::setImageOrientation — Встановлює орієнтацію зображення

### Опис

```methodsynopsis
public Imagick::setImageOrientation(int $orientation): bool
```

Встановлює орієнтацію зображення.

### Список параметрів

`orientation`

Одна из констант[ORIENTATION](imagick.constants.md#imagick.constants.orientation)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::setImageOrientation()\*\*\*\*

```php
<?php
// Кажется, ничего не делает
function setImageOrientation($imagePath, $orientationType) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageOrientation($orientationType);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
