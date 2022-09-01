---
navigation:
  - gmagick.setimagescene.html: '« Gmagick::setimagescene'
  - gmagick.setimageunits.html: 'Gmagick::setimageunits »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
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

Одна з констант [типа изображения](gmagick.constants.html#gmagick.constants.imagetype) `Gmagick::IMGTYPE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
