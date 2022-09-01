---
navigation:
  - gmagick.blurimage.html: '« Gmagick::blurimage'
  - gmagick.charcoalimage.html: 'Gmagick::charcoalimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::borderimage'
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

Викликає **GmagickException** у разі виникнення помилки.
