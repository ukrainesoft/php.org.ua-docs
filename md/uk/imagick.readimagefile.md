---
navigation:
  - imagick.readimageblob.md: '« Imagick::readImageBlob'
  - imagick.readimages.md: 'Imagick::readimages »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::readImageFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::readImageFile

(PECL imagick 2, PECL imagick 3)

Imagick::readImageFile — Читає зображення з відкритого дескриптора файлу

### Опис

```methodsynopsis
public Imagick::readImageFile(resource $filehandle, string $fileName = null): bool
```

Читає зображення із відкритого дескриптора файлу.

### Список параметрів

`filehandle`

`fileName`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
