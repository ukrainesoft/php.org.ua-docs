---
navigation:
  - gmagick.cropimage.md: '« Gmagick::cropimage'
  - gmagick.current.md: 'Gmagick::current »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::cropthumbnailimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Викликає **GmagickException**в случае возникновения ошибки.
