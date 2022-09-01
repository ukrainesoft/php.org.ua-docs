---
navigation:
  - imagick.painttransparentimage.html: '« Imagick::paintTransparentImage'
  - imagick.pingimageblob.html: 'Imagick::pingImageBlob »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::pingImage'
---
# Imagick::pingImage

(PECL imagick 2, PECL imagick 3)

Imagick::pingImage — Отримує основні атрибути зображення

### Опис

```methodsynopsis
public Imagick::pingImage(string $filename): bool
```

Метод можна використовувати для запиту ширини, висоти, розміру та формату зображення без зчитування всього зображення на згадку.

### Список параметрів

`filename`

Ім'я файлу, з якого потрібно прочитати інформацію.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
