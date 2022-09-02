---
navigation:
  - gmagick.setimagechanneldepth.md: '« Gmagick::setimagechanneldepth'
  - gmagick.setimagecompose.md: 'Gmagick::setimagecompose »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
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

Одна з констант [Цветового пространства](gmagick.constants.md#gmagick.constants.colorspace) `Gmagick::COLORSPACE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
