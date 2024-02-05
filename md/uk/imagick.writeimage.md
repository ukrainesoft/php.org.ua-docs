---
navigation:
  - imagick.whitethresholdimage.md: '« Imagick::whiteThresholdImage'
  - imagick.writeimagefile.md: 'Imagick::writeImageFile »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::writeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::writeImage

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::writeImage — Записує зображення за вказаним ім'ям файлу

### Опис

```methodsynopsis
public Imagick::writeImage(string $filename = NULL): bool
```

Записує зображення у вказане ім'я файлу. Якщо параметр імені файлу дорівнює NULL, зображення записується в ім'я файлу, встановлене за допомогою Imagick::readImage() або Imagick::setImageFilename().

### Список параметрів

`filename`

Назва файлу, куди записати зображення. Розширення імені файлу визначає тип файлу. Формат може бути примусово встановлений незалежно від розширення файлу, використовуючи префікс "format:", наприклад, "jpg:test.png".

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
