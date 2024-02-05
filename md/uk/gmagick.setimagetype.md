---
navigation:
  - gmagick.setimagescene.md: '« Gmagick::setimagescene'
  - gmagick.setimageunits.md: 'Gmagick::setimageunits »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagetype'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setimagetype

(PECL gmagick >= Unknown)

Gmagick::setimagetype — Встановлює тип зображення

### Опис

```methodsynopsis
public Gmagick::setimagetype(int $imgType): Gmagick
```

Встановлює тип зображення.

### Список параметрів

`imgType`

Одна из констант[типу зображення](gmagick.constants.md#gmagick.constants.imagetype) `Gmagick::IMGTYPE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
