---
navigation:
  - imagick.cropimage.md: '« Imagick::cropImage'
  - imagick.current.md: 'Imagick::current »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::cropThumbnailImage'
---
# Imagick::cropThumbnailImage

(PECL imagick 2, PECL imagick 3)

Imagick::cropThumbnailImage — Створює мініатюру, що обрізає.

### Опис

```methodsynopsis
public Imagick::cropThumbnailImage(int $width, int $height, bool $legacy = false): bool
```

Створює мініатюру фіксованого розміру, спочатку масштабуючи зображення вгору або вниз та обрізаючи вказану область від центру.

### Список параметрів

`width`

Ширина мініатюри

`height`

Висота мініатюри

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.
