---
navigation:
  - gmagick.magnifyimage.html: '« Gmagick::magnifyimage'
  - gmagick.medianfilterimage.html: 'Gmagick::medianfilterimage »'
  - index.html: PHP Manual
  - class.gmagick.html: Gmagick
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

Об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
