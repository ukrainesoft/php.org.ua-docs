---
navigation:
  - gmagick.readimage.html: '« Gmagick::readimage'
  - gmagick.readimagefile.html: 'Gmagick::readimagefile »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::readimageblob'
---
# Gmagick::readimageblob

(PECL gmagick >= Unknown)

Gmagick::readimageblob — Читає зображення з бінарного рядка

### Опис

```methodsynopsis
public Gmagick::readimageblob(string $imageContents, string $filename = ?): Gmagick
```

Читає зображення з бінарного рядка.

### Список параметрів

`imageContents`

Контент зображення.

`filename`

Назва файлу зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
