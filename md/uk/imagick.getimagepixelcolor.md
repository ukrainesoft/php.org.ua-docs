---
navigation:
  - imagick.getimagepage.md: '« Imagick::getImagePage'
  - imagick.getimageprofile.md: 'Imagick::getImageProfile »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImagePixelColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImagePixelColor

(PECL imagick 2, PECL imagick 3)

Imagick::getImagePixelColor — Повертає колір вказаного пікселя

### Опис

```methodsynopsis
public Imagick::getImagePixelColor(int $x, int $y): ImagickPixel
```

Повертає колір вказаного пікселя.

### Список параметрів

`x`

Координата x пікселя.

`y`

Координата у пікселя.

### Значення, що повертаються

Повертає екземпляр ImagickPixel для кольору у заданих координатах.

### Помилки

Викликає ImagickException у разі виникнення помилки.
