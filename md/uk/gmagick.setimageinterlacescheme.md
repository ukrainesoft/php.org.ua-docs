---
navigation:
  - gmagick.setimageindex.md: '« Gmagick::setimageindex'
  - gmagick.setimageiterations.md: 'Gmagick::setimageiterations »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setimageinterlacescheme'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setimageinterlacescheme

(PECL gmagick >= Unknown)

Gmagick::setimageinterlacescheme — Встановлює схему надстрокової розгортки зображення

### Опис

```methodsynopsis
public Gmagick::setimageinterlacescheme(int $interlace): Gmagick
```

Встановлює схему надстрокової розгортки зображення.

### Список параметрів

`interlace`

Одна из констант[схеми надрядкового зображення](gmagick.constants.md#gmagick.constants.interlace) `Gmagick::INTERLACE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
