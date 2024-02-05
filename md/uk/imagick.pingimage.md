---
navigation:
  - imagick.painttransparentimage.md: '« Imagick::paintTransparentImage'
  - imagick.pingimageblob.md: 'Imagick::pingImageBlob »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::pingImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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
