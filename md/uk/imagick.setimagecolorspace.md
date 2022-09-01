---
navigation:
  - imagick.setimagecolormapcolor.md: '« Imagick::setImageColormapColor'
  - imagick.setimagecompose.md: 'Imagick::setImageCompose »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageColorspace'
---
# Imagick::setImageColorspace

(PECL imagick 2, PECL imagick 3)

Imagick::setImageColorspace — Встановлює колірний простір зображення

### Опис

```methodsynopsis
public Imagick::setImageColorspace(int $colorspace): bool
```

Встановлює колірний простір зображення. Метод слід використовувати під час створення нових зображень. Щоб змінити колірний простір існуючого зображення, потрібно використовувати [Imagick::transformImageColorspace()](imagick.transformimagecolorspace.md)

### Список параметрів

`colorspace`

Одна з [COLORSPACE констант](imagick.constants.html#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
