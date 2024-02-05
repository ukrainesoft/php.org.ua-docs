---
navigation:
  - gmagick.addimage.md: '« Gmagick::addimage'
  - gmagick.annotateimage.md: 'Gmagick::annotateimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::addnoiseimage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::addnoiseimage

(PECL gmagick >= Unknown)

Gmagick::addnoiseimage — Додає випадковий шум до зображення

### Опис

```methodsynopsis
public Gmagick::addnoiseimage(int $noise_type): Gmagick
```

Додає випадковий шум зображення.

### Список параметрів

`noise_type`

Тип шума. Смотрите список[констант типу шуму](gmagick.constants.md#gmagick.constants.noise)

### Значення, що повертаються

Об'єкт Gmagick із доданим шумом.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
