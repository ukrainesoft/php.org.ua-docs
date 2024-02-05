---
navigation:
  - imagick.getimagetotalinkdensity.md: '« Imagick::getImageTotalInkDensity'
  - imagick.getimageunits.md: 'Imagick::getImageUnits »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageType

(PECL imagick 2, PECL imagick 3)

Imagick::getImageType — Повертає можливий тип зображення

### Опис

```methodsynopsis
public Imagick::getImageType(): int
```

Отримання можливого типу зображення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає тип зображення.

-   **`imagick::IMGTYPE_UNDEFINED`**
-   **`imagick::IMGTYPE_BILEVEL`**
-   **`imagick::IMGTYPE_GRAYSCALE`**
-   **`imagick::IMGTYPE_GRAYSCALEMATTE`**
-   **`imagick::IMGTYPE_PALETTE`**
-   **`imagick::IMGTYPE_PALETTEMATTE`**
-   **`imagick::IMGTYPE_TRUECOLOR`**
-   **`imagick::IMGTYPE_TRUECOLORMATTE`**
-   **`imagick::IMGTYPE_COLORSEPARATION`**
-   **`imagick::IMGTYPE_COLORSEPARATIONMATTE`**
-   **`imagick::IMGTYPE_OPTIMIZE`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
