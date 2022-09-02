---
navigation:
  - gmagick.setimagebordercolor.md: '« Gmagick::setimagebordercolor'
  - gmagick.setimagecolorspace.md: 'Gmagick::setimagecolorspace »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimagechanneldepth'
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

Одна з констант [канала](gmagick.constants.md#gmagick.constants.channel) `Gmagick::CHANNEL_*`

`depth`

Глибина зображення у бітах.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
