---
navigation:
  - imagick.quantizeimage.md: '« Imagick::quantizeImage'
  - imagick.queryfontmetrics.md: 'Imagick::queryFontMetrics »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::quantizeImages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::quantizeImages

(PECL imagick 2, PECL imagick 3)

Imagick::quantizeImages — Аналізує кольори у послідовності зображень

### Опис

```methodsynopsis
public Imagick::quantizeImages(    int $numberColors,    int $colorspace,    int $treedepth,    bool $dither,    bool $measureError): bool
```

### Список параметрів

`numberColors`

`colorspace`

`treedepth`

`dither`

`measureError`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
