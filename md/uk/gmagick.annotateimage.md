---
navigation:
  - gmagick.addnoiseimage.md: '« Gmagick::addnoiseimage'
  - gmagick.blurimage.md: 'Gmagick::blurimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::annotateimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::annotateimage

(PECL gmagick >= Unknown)

Gmagick::annotateimage — Підписати зображення текстом

### Опис

```methodsynopsis
public Gmagick::annotateimage(    GmagickDraw $GmagickDraw,    float $x,    float $y,    float $angle,    string $text): Gmagick
```

Підписати зображення тексту.

### Список параметрів

`GmagickDraw`

Об'єкт [GmagickDraw](class.gmagickdraw.md), що містить параметри для відображення тексту.

`x`

Горизонтальне зміщення лівого краю тексту в пікселях.

`y`

Вертикальне зміщення базової лінії тексту на пікселях.

`angle`

Кут під яким розміщувати текст.

`text`

Текст.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) з доданою інструкцією.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
