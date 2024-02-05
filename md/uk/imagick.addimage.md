---
navigation:
  - imagick.adaptivethresholdimage.md: '« Imagick::adaptiveThresholdImage'
  - imagick.addnoiseimage.md: 'Imagick::addNoiseImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::addImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::addImage

(PECL imagick 2, PECL imagick 3)

Imagick::addImage — Додає нове зображення до списку зображень об'єкту Imagick

### Опис

```methodsynopsis
public Imagick::addImage(Imagick $source): bool
```

Додає нове зображення до об'єкта Imagick із поточного положення вихідного об'єкта. Після цієї операції переміщається позиція ітератора до кінця списку.

### Список параметрів

`source`

Початковий об'єкт Imagick

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
