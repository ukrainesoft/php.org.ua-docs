---
navigation:
  - imagick.getimage.md: '« Imagick::getImage'
  - imagick.getimageartifact.md: 'Imagick::getImageArtifact »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageAlphaChannel'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getImageAlphaChannel

(PECL imagick 2 >= 2.3.0, PECL imagick 3)

Imagick::getImageAlphaChannel — Перевіряє, чи є зображення альфа-канал

### Опис

```methodsynopsis
public Imagick::getImageAlphaChannel(): bool
```

Повертає, чи є зображення альфа-канал.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`**, якщо зображення має альфа-канал і **`false`**, якщо ні, тобто. зображення RGB, а не RGBA чи CMYK, а не CMYKA.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| imagick 3.6.0 | Тепер повертає логічне значення (bool); раніше поверталося ціле число (int). |
