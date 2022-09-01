---
navigation:
  - gmagick.annotateimage.md: '« Gmagick::annotateimage'
  - gmagick.borderimage.md: 'Gmagick::borderimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::blurimage'
---
# Gmagick::blurimage

(PECL gmagick >= Unknown)

Gmagick::blurimage — Додати розмиття зображення

### Опис

```methodsynopsis
public Gmagick::blurimage(float $radius, float $sigma, int $channel = ?): Gmagick
```

Додати розмиття зображення.

### Список параметрів

`radius`

Радіус розмиття

`sigma`

Стандартне відхилення

### Значення, що повертаються

Розмитий об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
