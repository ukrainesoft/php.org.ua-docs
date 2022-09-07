---
navigation:
  - imagick.setbackgroundcolor.md: '« Imagick::setBackgroundColor'
  - imagick.setcompression.md: 'Imagick::setCompression »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
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

Одна з [констант COLORSPACE](imagick.constants.md#imagick.constants.colorspace)

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
