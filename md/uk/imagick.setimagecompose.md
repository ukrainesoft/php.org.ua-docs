---
navigation:
  - imagick.setimagecolorspace.md: '« Imagick::setImageColorspace'
  - imagick.setimagecompression.md: 'Imagick::setImageCompression »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageCompose'
---
# Imagick::setImageCompose

(PECL imagick 2, PECL imagick 3)

Imagick::setImageCompose — Встановлює оператор складеного зображення

### Опис

```methodsynopsis
public Imagick::setImageCompose(int $compose): bool
```

Встановлює оператор складеного зображення, корисний для вказівки, як складати ескіз зображення під час використання методу Imagick::montageImage().

### Список параметрів

`compose`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
