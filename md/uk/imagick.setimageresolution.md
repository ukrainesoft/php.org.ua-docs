---
navigation:
  - imagick.setimagerenderingintent.md: '« Imagick::setImageRenderingIntent'
  - imagick.setimagescene.md: 'Imagick::setImageScene »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageResolution'
---
# Imagick::setImageResolution

(PECL imagick 2, PECL imagick 3)

Imagick::setImageResolution — Встановлює роздільну здатність зображення

### Опис

```methodsynopsis
public Imagick::setImageResolution(float $x_resolution, float $y_resolution): bool
```

Встановлює роздільну здатність зображення.

### Список параметрів

`x_resolution`

`y_resolution`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::setImageResolution()****

```php
<?php
function setImageResolution($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageResolution(50, 50);

    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
