---
navigation:
  - imagick.getimageredprimary.md: '« Imagick::getImageRedPrimary'
  - imagick.getimagerenderingintent.md: 'Imagick::getImageRenderingIntent »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageRegion'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageRegion

(PECL imagick 2, PECL imagick 3)

Imagick::getImageRegion — Витягує область зображення

### Опис

```methodsynopsis
public Imagick::getImageRegion(    int $width,    int $height,    int $x,    int $y): Imagick
```

Витягує область зображення та повертає її у вигляді нового об'єкта Imagick.

### Список параметрів

`width`

Ширина вилученої області.

`height`

Висота витягнутої області.

`x`

Координата X лівого верхнього кута одержаної області.

`y`

Координата Y лівого верхнього кута видобутої області.

### Значення, що повертаються

Витягує область зображення та повертає її у вигляді нової палички.

### Помилки

Викликає ImagickException у разі виникнення помилки.
