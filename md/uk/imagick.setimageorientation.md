---
navigation:
  - imagick.setimageopacity.md: '« Imagick::setImageOpacity'
  - imagick.setimagepage.md: 'Imagick::setImagePage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageOrientation'
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

Одна з констант [ORIENTATION](imagick.constants.md#imagick.constants.orientation)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageOrientation()****

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
