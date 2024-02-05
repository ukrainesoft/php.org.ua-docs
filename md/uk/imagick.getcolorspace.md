---
navigation:
  - imagick.gaussianblurimage.md: '« Imagick::gaussianBlurImage'
  - imagick.getcompression.md: 'Imagick::getCompression »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getColorspace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getColorspace

(PECL imagick 3)

Imagick::getColorspace — Повертає палітру кольорів

### Опис

```methodsynopsis
public Imagick::getColorspace(): int
```

Повертає значення глобальної палітри кольорів. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.5.7 або старшим.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число, яке можна порівняти з [константами COLORSPACE](imagick.constants.md#imagick.constants.colorspace)
