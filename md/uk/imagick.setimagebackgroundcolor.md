---
navigation:
  - imagick.setimageattribute.md: '« Imagick::setImageAttribute'
  - imagick.setimagebias.md: 'Imagick::setImageBias »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setImageBackgroundColor'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setImageBackgroundColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageBackgroundColor — Встановлює колір тла зображення

### Опис

```methodsynopsis
public Imagick::setImageBackgroundColor(mixed $background): bool
```

Встановлює колір тла зображення.

### Список параметрів

`background`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяє використовувати рядок, що представляє колір, як параметр. Попередні версії дозволяли використовувати лише об'єкт ImagickPixel. |
