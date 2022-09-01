---
navigation:
  - gmagick.normalizeimage.md: '« Gmagick::normalizeimage'
  - gmagick.previousimage.md: 'Gmagick::previousimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::oilpaintimage'
---
# Gmagick::oilpaintimage

(PECL gmagick >= Unknown)

Gmagick::oilpaintimage — Імітує ефект картини олією

### Опис

```methodsynopsis
public Gmagick::oilpaintimage(
      float
       $radius
    ): Gmagick
```

Застосовує фільтр із спеціальним ефектом, що імітує картину олією. Кожен піксель замінюється кольором, що найчастіше зустрічається в круговій області, що визначається радіусом.

### Список параметрів

`radius`

Радіус кругової околиці.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
