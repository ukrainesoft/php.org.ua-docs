---
navigation:
  - imagick.getimageresolution.md: '« Imagick::getImageResolution'
  - imagick.getimagescene.md: 'Imagick::getImageScene »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImagesBlob'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImagesBlob

(PECL imagick 2, PECL imagick 3)

Imagick::getImagesBlob — Повертає всі послідовності зображення у вигляді великого двійкового об'єкта

### Опис

```methodsynopsis
public Imagick::getImagesBlob(): string
```

Реалізує формати зображень безпосередньо на згадку. Метод повертає всі послідовності зображень у вигляді рядка. Формат зображення визначає формат великого двійкового об'єкта, що повертається (GIF, JPEG, PNG і т.д.). Щоб повернути інший формат зображення, використовуйте Imagick::setImageFormat().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок, який містить зображення. У разі виникнення помилки викидає виняток ImagickException.
