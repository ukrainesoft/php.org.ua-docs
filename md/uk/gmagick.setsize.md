---
navigation:
  - gmagick.setsamplingfactors.md: '« Gmagick::setsamplingfactors'
  - gmagick.shearimage.md: 'Gmagick::shearimage »'
  - index.md: PHP Manual
  - class.gmagick.md: Gmagick
title: 'Gmagick::setsize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Gmagick::setsize

(PECL gmagick >= Unknown)

Gmagick::setsize — Встановлює розмір об'єкта Gmagick

### Опис

```methodsynopsis
public Gmagick::setsize(int $columns, int $rows): Gmagick
```

Встановлює розмір об'єкта Gmagick. Встановіть його, перш ніж читати сирий формат зображення, такий як **`Gmagick::COLORSPACE_RGB`** **`Gmagick::COLORSPACE_GRAY`** або **`Gmagick::COLORSPACE_CMYK`**

### Список параметрів

`columns`

Ширина у пікселях.

`rows`

Висота у пікселях.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.md) у разі успішного виконання.

### Помилки

Викликає **GmagickException**в случае возникновения ошибки.
