---
navigation:
  - imagick.decipherimage.html: '« Imagick::decipherImage'
  - imagick.deleteimageartifact.html: 'Imagick::deleteImageArtifact »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::deconstructImages'
---
# Imagick::deconstructImages

(PECL imagick 2, PECL imagick 3)

Imagick::deconstructImages — Повертає певні піксельні відмінності між зображеннями

### Опис

```methodsynopsis
public Imagick::deconstructImages(): Imagick
```

Порівнює кожне зображення з наступним у послідовності і повертає максимальну область, що обмежує будь-яких виявлених відмінностей пікселів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий об'єкт Imagick у разі успішного виконання.

### Помилки

Викликає ImagickException у разі виникнення помилки.
