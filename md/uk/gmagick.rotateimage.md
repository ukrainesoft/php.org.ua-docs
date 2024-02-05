---
navigation:
  - gmagick.rollimage.md: '« Gmagick::rollimage'
  - gmagick.scaleimage.md: 'Gmagick::scaleimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::rotateimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::rotateimage

(PECL gmagick >= Unknown)

Gmagick::rotateimage — Повертає зображення

### Опис

```methodsynopsis
public Gmagick::rotateimage(mixed $color, float $degrees): Gmagick
```

Повертає зображення на вказану кількість градусів. Порожні трикутники, що залишилися від повороту зображення, заповнюються кольором тла.

### Список параметрів

`color`

Піксель фону.

`degrees`

Число градусів для повороту зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
