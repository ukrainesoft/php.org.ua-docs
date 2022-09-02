---
navigation:
  - gmagick.setimagetype.md: '« Gmagick::setimagetype'
  - gmagick.setimagewhitepoint.md: 'Gmagick::setimagewhitepoint »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimageunits'
---
# Gmagick::setimageunits

(PECL gmagick >= Unknown)

Gmagick::setimageunits — Встановлює одиниці роздільної здатності зображення

### Опис

```methodsynopsis
public Gmagick::setimageunits(int $resolution): Gmagick
```

Встановлює одиниці роздільної здатності зображення.

### Список параметрів

`resolution`

Одна з констант [разрешения](gmagick.constants.md#gmagick.constants.resolution) `Gmagick::RESOLUTION_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
