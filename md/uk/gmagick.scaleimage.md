---
navigation:
  - gmagick.rotateimage.md: '« Gmagick::rotateimage'
  - gmagick.separateimagechannel.md: 'Gmagick::separateimagechannel »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::scaleimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::scaleimage

(PECL gmagick >= Unknown)

Gmagick::scaleimage — Масштабує розмір зображення

### Опис

```methodsynopsis
public Gmagick::scaleimage(int $width, int $height, bool $fit = false): Gmagick
```

Масштабує розмір зображення до розмірів. Інший параметр буде розрахований, якщо як будь-який з параметрів буде переданий 0.

### Список параметрів

`width`

Кількість стовпців у масштабованому зображенні.

`height`

Кількість рядків у масштабованому зображенні.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
