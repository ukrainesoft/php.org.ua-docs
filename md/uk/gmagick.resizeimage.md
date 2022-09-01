---
navigation:
  - gmagick.resampleimage.html: '« Gmagick::resampleimage'
  - gmagick.rollimage.html: 'Gmagick::rollimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
title: 'Gmagick::resizeimage'
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

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
