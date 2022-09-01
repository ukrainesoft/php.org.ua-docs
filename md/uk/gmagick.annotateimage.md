---
navigation:
  - gmagick.addnoiseimage.html: '« Gmagick::addnoiseimage'
  - gmagick.blurimage.html: 'Gmagick::blurimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::annotateimage'
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

Викликає **GmagickException** у разі виникнення помилки.
