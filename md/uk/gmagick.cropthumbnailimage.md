---
navigation:
  - gmagick.cropimage.md: '« Gmagick::cropimage'
  - gmagick.current.md: 'Gmagick::current »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::cropthumbnailimage'
---
# Gmagick::cropthumbnailimage

(PECL gmagick >= Unknown)

Gmagick::cropthumbnailimage — Створення обрізаного зменшеного зображення

### Опис

```methodsynopsis
public Gmagick::cropthumbnailimage(int $width, int $height): Gmagick
```

Створює зменшене зображення фіксованого розміру, спочатку застосовуючи масштабування, а потім вирізаючи необхідну область із центру.

### Список параметрів

`width`

Ширина цільового зображення.

`height`

Висота цільового зображення.

### Значення, що повертаються

Об'єкт, що вийшов [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.
