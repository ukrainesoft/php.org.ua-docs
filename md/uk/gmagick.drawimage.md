---
navigation:
  - gmagick.destroy.md: '« Gmagick::destroy'
  - gmagick.edgeimage.md: 'Gmagick::edgeimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::drawimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::drawimage

(PECL gmagick >= Unknown)

Gmagick::drawimage — Відображає об'єкт GmagickDraw на поточному зображенні

### Опис

```methodsynopsis
public Gmagick::drawimage(GmagickDraw $GmagickDraw): Gmagick
```

Відображає об'єкт [GmagickDraw](class.gmagickdraw.md)на текущем изображении

### Список параметрів

`GmagickDraw`

Операції малювання для відображення зображення.

### Значення, що повертаються

Намальований об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
