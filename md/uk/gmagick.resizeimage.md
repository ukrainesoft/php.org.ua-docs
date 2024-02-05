---
navigation:
  - gmagick.resampleimage.md: '« Gmagick::resampleimage'
  - gmagick.rollimage.md: 'Gmagick::rollimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::resizeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::resizeimage

(PECL gmagick >= Unknown)

Gmagick::resizeimage — Масштабування зображення

### Опис

```methodsynopsis
public Gmagick::resizeimage(    int $width,    int $height,    int $filter,    float $blur,    bool $fit = false): Gmagick
```

Масштабує зображення до бажаних розмірів за допомогою фільтра.

### Список параметрів

`width`

Кількість стовпців у масштабованому зображенні.

`height`

Кількість рядків у масштабованому зображенні.

`filter`

Фільтр зображень для використання.

`blur`

Коефіцієнт розмиття, де більше значення більше 1 робить зображення більш розмитим, значення менше 1 менш розмитим.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
