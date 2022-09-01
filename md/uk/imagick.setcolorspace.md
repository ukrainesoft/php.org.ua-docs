---
navigation:
  - imagick.setbackgroundcolor.html: '« Imagick::setBackgroundColor'
  - imagick.setcompression.html: 'Imagick::setCompression »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setColorspace'
---
# Imagick::setColorspace

(PECL imagick 3)

Imagick::setColorspace — Встановлює колірний простір

### Опис

```methodsynopsis
public Imagick::setColorspace(int $COLORSPACE): bool
```

Встановлює значення глобального кольору для об'єкта. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.5.7 або старшим.

### Список параметрів

`COLORSPACE`

Одна з [констант COLORSPACE](imagick.constants.html#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
