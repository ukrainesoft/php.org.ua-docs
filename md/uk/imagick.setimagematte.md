---
navigation:
  - imagick.setimageiterations.md: '« Imagick::setImageIterations'
  - imagick.setimagemattecolor.md: 'Imagick::setImageMatteColor »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
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
