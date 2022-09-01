---
navigation:
  - gmagick.setimagechanneldepth.html: '« Gmagick::setimagechanneldepth'
  - gmagick.setimagecompose.html: 'Gmagick::setimagecompose »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::setimagecolorspace'
---
# Gmagick::setimagecolorspace

(PECL gmagick >= Unknown)

Gmagick::setimagecolorspace — Встановлює колірний простір зображення

### Опис

```methodsynopsis
public Gmagick::setimagecolorspace(int $colorspace): Gmagick
```

Встановлює колірний простір зображення.

### Список параметрів

`colorspace`

Одна з констант [Цветового пространства](gmagick.constants.html#gmagick.constants.colorspace) `Gmagick::COLORSPACE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
