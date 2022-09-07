---
navigation:
  - gmagick.readimage.md: '« Gmagick::readimage'
  - gmagick.readimagefile.md: 'Gmagick::readimagefile »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
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

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
