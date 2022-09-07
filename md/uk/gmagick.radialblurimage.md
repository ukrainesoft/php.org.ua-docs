---
navigation:
  - gmagick.queryformats.md: '« Gmagick::queryformats'
  - gmagick.raiseimage.md: 'Gmagick::raiseimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::radialblurimage'
---
# Gmagick::radialblurimage

(PECL gmagick >= Unknown)

Gmagick::radialblurimage — Застосовує радіальне розмиття до зображення

### Опис

```methodsynopsis
public Gmagick::radialblurimage(float $angle, int $channel = Gmagick::CHANNEL_DEFAULT): Gmagick
```

Застосовує радіальне розмиття зображення.

### Список параметрів

`angle`

Кут розмиття в градусах.

`channel`

Пов'язаний канал.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
