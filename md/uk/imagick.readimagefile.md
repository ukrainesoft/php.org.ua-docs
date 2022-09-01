---
navigation:
  - imagick.readimageblob.html: '« Imagick::readImageBlob'
  - imagick.readimages.html: 'Imagick::readimages »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::readImageFile'
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
