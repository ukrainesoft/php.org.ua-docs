---
navigation:
  - gmagick.motionblurimage.md: '« Gmagick::motionblurimage'
  - gmagick.nextimage.md: 'Gmagick::nextimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::newimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::newimage

(PECL gmagick >= Unknown)

Gmagick::newimage — Створює нове зображення

### Опис

```methodsynopsis
public Gmagick::newimage(    int $width,    int $height,    string $background,    string $format = ?): Gmagick
```

Створює нове зображення із зазначеним фоновим кольором.

### Список параметрів

`width`

Ширина нового зображення.

`height`

Висота нового зображення.

`background`

Колір фону, який використовується для цього зображення у вигляді числа з плаваючою точкою.

`format`

Формат зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
