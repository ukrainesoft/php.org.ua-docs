---
navigation:
  - imagick.setimageiterations.html: '« Imagick::setImageIterations'
  - imagick.setimagemattecolor.html: 'Imagick::setImageMatteColor »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setImageMatte'
---
# Imagick::setImageMatte

(PECL imagick 2, PECL imagick 3)

Imagick::setImageMatte — Встановлює матовий канал зображення

### Опис

```methodsynopsis
public Imagick::setImageMatte(bool $matte): bool
```

Встановлює матовий канал зображення. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`matte`

Значення true активує матовий канал, false – відключає.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
