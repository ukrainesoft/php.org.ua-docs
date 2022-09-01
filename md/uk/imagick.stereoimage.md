---
navigation:
  - imagick.steganoimage.html: '« Imagick::steganoImage'
  - imagick.stripimage.html: 'Imagick::stripImage »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::stereoImage'
---
# Imagick::stereoImage

(PECL imagick 2, PECL imagick 3)

Imagick::stereoImage — Об'єднує два зображення

### Опис

```methodsynopsis
public Imagick::stereoImage(Imagick $offset_wand): bool
```

Об'єднує два зображення та створює одне зображення, яке є складовою лівого та правого зображення стереопари.

### Список параметрів

`offset_wand`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
