---
navigation:
  - gmagick.cyclecolormapimage.md: '« Gmagick::cyclecolormapimage'
  - gmagick.despeckleimage.md: 'Gmagick::despeckleimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::deconstructimages'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::deconstructimages

(PECL gmagick >= Unknown)

Gmagick::deconstructimages — Повертає певні піксельні відмінності між зображеннями

### Опис

```methodsynopsis
public Gmagick::deconstructimages(): Gmagick
```

Порівнює кожне зображення з наступним у послідовності і повертає максимальну область, що обмежує будь-яких виявлених відмінностей пікселів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає новий об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
