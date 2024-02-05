---
navigation:
  - gmagick.resizeimage.md: '« Gmagick::resizeimage'
  - gmagick.rotateimage.md: 'Gmagick::rotateimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::rollimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::rollimage

(PECL gmagick >= Unknown)

Gmagick::rollimage — Зміщує зображення

### Опис

```methodsynopsis
public Gmagick::rollimage(int $x, int $y): Gmagick
```

Зміщує зображення відповідно до x та y.

### Список параметрів

`x`

Зміщення по осі x.

`y`

Зміщення осі y.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
