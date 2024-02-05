---
navigation:
  - gmagick.setimagechanneldepth.md: '« Gmagick::setimagechanneldepth'
  - gmagick.setimagecompose.md: 'Gmagick::setimagecompose »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagecolorspace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Одна из констант[Колірного простору](gmagick.constants.md#gmagick.constants.colorspace) `Gmagick::COLORSPACE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
