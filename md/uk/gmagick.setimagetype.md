---
navigation:
  - gmagick.setimagescene.md: '« Gmagick::setimagescene'
  - gmagick.setimageunits.md: 'Gmagick::setimageunits »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagetype'
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

Одна з констант [типа изображения](gmagick.constants.md#gmagick.constants.imagetype) `Gmagick::IMGTYPE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
