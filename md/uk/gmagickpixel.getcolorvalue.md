---
navigation:
  - gmagickpixel.getcolorcount.md: '« GmagickPixel::getcolorcount'
  - gmagickpixel.setcolor.md: 'GmagickPixel::setcolor »'
  - index.md: PHP Manual
  - class.gmagickpixel.md: GmagickPixel
title: 'GmagickPixel::getcolorvalue'
---
# GmagickPixel::getcolorvalue

(PECL gmagick >= Unknown)

GmagickPixel::getcolorvalue — Повертає нормалізоване значення для заданого каналу кольорів

### Опис

```methodsynopsis
public GmagickPixel::getcolorvalue(int $color): float
```

Повертає нормалізоване значення для заданого каналу кольору у вигляді числа з плаваючою точкою в діапазоні від 0 до 1.

### Список параметрів

`color`

Колірний канал. Одна із констант колірних каналів Gmagick.

### Значення, що повертаються

Повертає нормалізоване значення для заданого каналу кольору, або, у разі виникнення помилки, викидає виняток **GmagickPixelException**
