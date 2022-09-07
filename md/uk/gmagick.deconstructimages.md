---
navigation:
  - gmagick.cyclecolormapimage.md: '« Gmagick::cyclecolormapimage'
  - gmagick.despeckleimage.md: 'Gmagick::despeckleimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::deconstructimages'
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

Викликає **GmagickException** у разі виникнення помилки.
