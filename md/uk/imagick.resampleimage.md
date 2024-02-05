---
navigation:
  - imagick.render.md: '« Imagick::render'
  - imagick.resetimagepage.md: 'Imagick::resetImagePage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::resampleImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::resampleImage

(PECL imagick 2, PECL imagick 3)

Imagick::resampleImage — Перетворює зображення до потрібної роздільної здатності

### Опис

```methodsynopsis
public Imagick::resampleImage(    float $x_resolution,    float $y_resolution,    int $filter,    float $blur): bool
```

Перетворює зображення до потрібної роздільної здатності.

### Список параметрів

`x_resolution`

`y_resolution`

`filter`

`blur`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад использования метода**Imagick::resampleImage()\*\*\*\*

```php
<?php
function resampleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->resampleImage(200, 200, \Imagick::FILTER_LANCZOS, 1);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
