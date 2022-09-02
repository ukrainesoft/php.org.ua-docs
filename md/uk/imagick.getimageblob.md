---
navigation:
  - imagick.getimagebackgroundcolor.md: '« Imagick::getImageBackgroundColor'
  - imagick.getimageblueprimary.md: 'Imagick::getImageBluePrimary »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageBlob'
---
# Imagick::getImageBlob

(PECL imagick 2, PECL imagick 3)

Imagick::getImageBlob — Повертає послідовність зображень у вигляді BLOB

### Опис

```methodsynopsis
public Imagick::getImageBlob(): string
```

Реалізує формати зображень безпосередньо на згадку. Повертає послідовність зображень у вигляді рядка. Формат зображення визначає формат BLOB-об'єкта, що повертається (GIF, JPEG, PNG і т.д.). Щоб повернути інший формат зображення, використовуйте Imagick::setImageFormat().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, який містить зображення.

### Помилки

Викликає ImagickException у разі виникнення помилки.
