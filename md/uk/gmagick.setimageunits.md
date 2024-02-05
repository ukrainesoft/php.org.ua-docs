---
navigation:
  - gmagick.setimagetype.md: '« Gmagick::setimagetype'
  - gmagick.setimagewhitepoint.md: 'Gmagick::setimagewhitepoint »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimageunits'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Одна из констант[дозволу](gmagick.constants.md#gmagick.constants.resolution) `Gmagick::RESOLUTION_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
