---
navigation:
  - gmagick.haspreviousimage.md: '« Gmagick::haspreviousimage'
  - gmagick.labelimage.md: 'Gmagick::labelimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::implodeimage'
---
# Gmagick::implodeimage

(PECL gmagick >= Unknown)

Gmagick::implodeimage — Створює копію зображення

### Опис

```methodsynopsis
public Gmagick::implodeimage(float $radius): mixed
```

Створює нове зображення, яке є копією існуючого з пікселями, "стиснутими" на зазначений відсоток.

### Список параметрів

`radius`

Радіус стиснення.

### Значення, що повертаються

Повертає стислий об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
