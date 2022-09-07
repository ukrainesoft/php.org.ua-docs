---
navigation:
  - gmagick.magnifyimage.md: '« Gmagick::magnifyimage'
  - gmagick.medianfilterimage.md: 'Gmagick::medianfilterimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::mapimage'
---
# Gmagick::mapimage

(PECL gmagick >= Unknown)

Gmagick::mapimage — Замінює кольори зображення на найближчий колір із еталонного зображення

### Опис

```methodsynopsis
public Gmagick::mapimage(gmagick $gmagick, bool $dither): Gmagick
```

Замінює кольори зображення на найближчий колір із еталонного зображення.

### Список параметрів

`gmagick`

Еталонне зображення.

`dither`

Встановіть для цього цілого числа значення, відмінне від нуля, щоб розмити зображення, що відображається.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
