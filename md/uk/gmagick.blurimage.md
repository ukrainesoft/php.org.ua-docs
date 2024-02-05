---
navigation:
  - gmagick.annotateimage.md: '« Gmagick::annotateimage'
  - gmagick.borderimage.md: 'Gmagick::borderimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::blurimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
