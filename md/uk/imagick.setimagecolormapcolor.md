---
navigation:
  - imagick.setimageclipmask.md: '« Imagick::setImageClipMask'
  - imagick.setimagecolorspace.md: 'Imagick::setImageColorspace »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageColormapColor'
---
# Imagick::setImageColormapColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageColormapColor — Встановлює колір вказаного індексу картки

### Опис

```methodsynopsis
public Imagick::setImageColormapColor(int $index, ImagickPixel $color): bool
```

Встановлює колір зазначеного індексу карти кольорів.

### Список параметрів

`index`

`color`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
