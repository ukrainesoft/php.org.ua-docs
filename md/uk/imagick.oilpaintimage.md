---
navigation:
  - imagick.normalizeimage.md: '« Imagick::normalizeImage'
  - imagick.opaquepaintimage.md: 'Imagick::opaquePaintImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::oilPaintImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::oilPaintImage

(PECL imagick 2, PECL imagick 3)

Imagick::oilPaintImage — Імітує картину олією

### Опис

```methodsynopsis
public Imagick::oilPaintImage(float $radius): bool
```

Застосовує фільтр із спеціальним ефектом, що імітує картину олією. Кожен піксель замінюється кольором, що найчастіше зустрічається в круговій області, що визначається радіусом.

### Список параметрів

`radius`

Радіус кругової області.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::oilPaintImage()\*\*\*\*

```php
<?php
function oilPaintImage($imagePath, $radius) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->oilPaintImage($radius);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
