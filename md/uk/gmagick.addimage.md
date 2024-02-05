---
navigation:
  - class.gmagick.md: « Gmagick
  - gmagick.addnoiseimage.md: 'Gmagick::addnoiseimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::addimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::addimage

(PECL gmagick >= Unknown)

Gmagick::addimage — Додавання нового зображення до списку зображень об'єкта Gmagick

### Опис

```methodsynopsis
public Gmagick::addimage(Gmagick $source): Gmagick
```

Додавання нового зображення до об'єкта Gmagick з поточної позиції джерела. Після додавання позиції ітератор зміщується в кінець списку.

### Список параметрів

`source`

Об'єкт джерело Gmagick

### Значення, що повертаються

Об'єкт Gmagick із доданим зображенням

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
