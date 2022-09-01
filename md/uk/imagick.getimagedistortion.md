---
navigation:
  - imagick.getimagedispose.md: '« Imagick::getImageDispose'
  - imagick.getimageextrema.md: 'Imagick::getImageExtrema »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageDistortion'
---
# Imagick::getImageDistortion

(PECL imagick 2, PECL imagick 3)

Imagick::getImageDistortion — Порівнює зображення з відновленим зображенням

### Опис

```methodsynopsis
public Imagick::getImageDistortion(MagickWand $reference, int $metric): float
```

Порівнює зображення з відновленим зображенням та повертає вказаний показник спотворення.

### Список параметрів

`reference`

Об'єкт Imagick для порівняння.

`metric`

Одна з [констант типа METRIC](imagick.constants.html#imagick.constants.metric)

### Значення, що повертаються

Повертає показник спотворення, використаний для зображення (або найкраще припущення).

### Помилки

Викликає ImagickException у разі виникнення помилки.
