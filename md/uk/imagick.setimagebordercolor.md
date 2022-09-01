---
navigation:
  - imagick.setimageblueprimary.html: '« Imagick::setImageBluePrimary'
  - imagick.setimagechanneldepth.html: 'Imagick::setImageChannelDepth »'
  - index.html: PHP Manual
  - class.imagick.html: Imagick
title: 'Imagick::setImageBorderColor'
---
# Imagick::setImageBorderColor

(PECL imagick 2, PECL imagick 3)

Imagick::setImageBorderColor — Встановлює колір зображення.

### Опис

```methodsynopsis
public Imagick::setImageBorderColor(mixed $border): bool
```

Встановлює колір кадру зображення.

### Список параметрів

`border`

Колір рамки

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL imagick 2.1.0 | Тепер дозволяється передавати рядок, який представляє колір як параметр. Попередні версії допускають лише об'єкт ImagickPixel. |
