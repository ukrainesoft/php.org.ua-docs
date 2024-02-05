---
navigation:
  - gmagickpixel.setcolor.md: '« GmagickPixel::setcolor'
  - book.imagick.md: ImageMagick »
  - index.md: PHP Manual
  - class.gmagickpixel.md: GmagickPixel
title: 'GmagickPixel::setcolorvalue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GmagickPixel::setcolorvalue

(PECL gmagick >= Unknown)

GmagickPixel::setcolorvalue — Встановити нормалізоване значення колірного каналу

### Опис

```methodsynopsis
public GmagickPixel::setcolorvalue(int $color, float $value): GmagickPixel
```

Встановлює нормалізоване значення колірного каналу. Значення має бути числом з плаваючою точкою (float) в діапазоні від 0 до 1. Також ця функція може використовуватися для визначення каналу прозорості об'єкта [GmagickPixel](class.gmagickpixel.md)

### Список параметрів

`color`

Колірний канал. Одна із констант колірних каналів Gmagick.

`value`

Значення, що встановлюється. Число з точкою, що плаває, в діапазоні від 0 до 1.

### Значення, що повертаються

Об'єкт [GmagickPixel](class.gmagickpixel.md) у разі успішного виконання.
