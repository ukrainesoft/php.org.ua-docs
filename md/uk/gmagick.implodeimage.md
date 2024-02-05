---
navigation:
  - gmagick.haspreviousimage.md: '« Gmagick::haspreviousimage'
  - gmagick.labelimage.md: 'Gmagick::labelimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::implodeimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
