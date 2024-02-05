---
navigation:
  - gmagick.blurimage.md: '« Gmagick::blurimage'
  - gmagick.charcoalimage.md: 'Gmagick::charcoalimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::borderimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::borderimage

(PECL gmagick >= Unknown)

Gmagick::borderimage — Додати рамку до зображення

### Опис

```methodsynopsis
public Gmagick::borderimage(GmagickPixel $color, int $width, int $height): Gmagick
```

Додати рамку зображення. Колір рамки задається рядком або кольором фону об'єкта [GmagickPixel](class.gmagickpixel.md)

### Список параметрів

`color`

Об'єкт [GmagickPixel](class.gmagickpixel.md) object або рядок, що визначає колір рамки.

`width`

Товщина кадру.

`height`

Висота кадру.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) з доданою рамкою.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
