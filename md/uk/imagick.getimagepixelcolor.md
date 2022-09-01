---
navigation:
  - imagick.getimagepage.md: '« Imagick::getImagePage'
  - imagick.getimageprofile.md: 'Imagick::getImageProfile »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImagePixelColor'
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

Повертає екземпляр ImagickPixel для кольору в заданих координатах.

### Помилки

Викликає ImagickException у разі виникнення помилки.
