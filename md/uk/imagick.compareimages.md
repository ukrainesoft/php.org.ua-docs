---
navigation:
  - imagick.compareimagelayers.md: '« Imagick::compareImageLayers'
  - imagick.compositeimage.md: 'Imagick::compositeImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::compareImages'
---
# Imagick::compareImages

(PECL imagick 2, PECL imagick 3)

Imagick::compareImages — Порівнює зображення з відновленим зображенням

### Опис

```methodsynopsis
public Imagick::compareImages(Imagick $compare, int $metric): array
```

Повертає масив, що містить відновлене зображення та різницю між зображеннями.

### Список параметрів

`compare`

Зображення для порівняння.

`metric`

Вкажіть допустиму константу типу метрики. Дивіться список [констант метрики](imagick.constants.md#imagick.constants.metric)

### Значення, що повертаються

Повертає масив, що містить відновлене зображення та різницю між зображеннями.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **Imagick::compareImages()****

Порівняння зображення та відображення відновленого зображення

```php
<?php

$image1 = new imagick("image1.png");
$image2 = new imagick("image2.png");

$result = $image1->compareImages($image2, Imagick::METRIC_MEANSQUAREERROR);
$result[0]->setImageFormat("png");

header("Content-Type: image/png");
echo $result[0];

?>
```
