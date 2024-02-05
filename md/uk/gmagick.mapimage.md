---
navigation:
  - gmagick.magnifyimage.md: '« Gmagick::magnifyimage'
  - gmagick.medianfilterimage.md: 'Gmagick::medianfilterimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::mapimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
