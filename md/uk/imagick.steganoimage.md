---
navigation:
  - imagick.statisticimage.md: '« Imagick::statisticImage'
  - imagick.stereoimage.md: 'Imagick::stereoImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::steganoImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::steganoImage

(PECL imagick 2, PECL imagick 3)

Imagick::steganoImage — Приховує цифровий водяний знак у зображенні

### Опис

```methodsynopsis
public Imagick::steganoImage(Imagick $watermark_wand, int $offset): Imagick
```

Приховує цифровий водяний знак у зображенні. Відновіть прихований водяний знак пізніше, щоб довести справжність зображення. Зсув визначає початкову позицію на зображенні, щоб приховати водяний знак.

### Список параметрів

`watermark_wand`

`offset`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
