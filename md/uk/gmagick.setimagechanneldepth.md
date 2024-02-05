---
navigation:
  - gmagick.setimagebordercolor.md: '« Gmagick::setimagebordercolor'
  - gmagick.setimagecolorspace.md: 'Gmagick::setimagecolorspace »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagechanneldepth'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setimagechanneldepth

(PECL gmagick >= Unknown)

Gmagick::setimagechanneldepth — Встановлює глибину певного каналу зображення

### Опис

```methodsynopsis
public Gmagick::setimagechanneldepth(int $channel, int $depth): Gmagick
```

Встановлює глибину певного каналу зображення.

### Список параметрів

`channel`

Одна из констант[каналу](gmagick.constants.md#gmagick.constants.channel) `Gmagick::CHANNEL_*`

`depth`

Глибина зображення у бітах.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
