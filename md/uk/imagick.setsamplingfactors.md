---
navigation:
  - imagick.setresourcelimit.md: '« Imagick::setResourceLimit'
  - imagick.setsize.md: 'Imagick::setSize »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setSamplingFactors'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setSamplingFactors

(PECL imagick 2, PECL imagick 3)

Imagick::setSamplingFactors — Встановлює коефіцієнти вибірки зображень

### Опис

```methodsynopsis
public Imagick::setSamplingFactors(array $factors): bool
```

Встановлює коефіцієнти вибірки зображень.

### Список параметрів

`factors`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** Imagick::setSamplingFactors()\*\*\*\*

```php
<?php
function setSamplingFactors($imagePath) {

    $imagePath = "../imagick/images/FineDetail.png";
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->setImageFormat('jpg');
    $imagick->setSamplingFactors(array('2x2', '1x1', '1x1'));

    $compressed = $imagick->getImageBlob();


    $reopen = new \Imagick();
    $reopen->readImageBlob($compressed);

    $reopen->resizeImage(
        $reopen->getImageWidth() * 4,
        $reopen->getImageHeight() * 4,
        \Imagick::FILTER_POINT,
        1
    );

    header("Content-Type: image/jpg");
    echo $reopen->getImageBlob();
}

?>
```
