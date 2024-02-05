---
navigation:
  - gmagick.commentimage.md: '« Gmagick::commentimage'
  - gmagick.construct.md: 'Gmagick::\_\_construct »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::compositeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::compositeimage

(PECL gmagick >= Unknown)

Gmagick::compositeimage — Накладає одне зображення на інше

### Опис

```methodsynopsis
public Gmagick::compositeimage(    Gmagick $source,    int $COMPOSE,    int $x,    int $y): Gmagick
```

Накладає одне зображення на інше із зазначеним усуненням.

### Список параметрів

`source`

Об'єкт [Gmagick](class.gmagick.md), що містить складне зображення.

`compose`

Композитний оператор.

`x`

Усунення стовпця складеного зображення.

`y`

Зміщення рядка складеного зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) із композиціями.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
