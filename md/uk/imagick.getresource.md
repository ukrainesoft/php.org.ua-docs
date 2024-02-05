---
navigation:
  - imagick.getreleasedate.md: '« Imagick::getReleaseDate'
  - imagick.getresourcelimit.md: 'Imagick::getResourceLimit »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getResource'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getResource

(PECL imagick 2, PECL imagick 3)

Imagick::getResource — Повертає розмір пам'яті вказаного ресурсу.

### Опис

```methodsynopsis
public static Imagick::getResource(int $type): int
```

Повертає розмір пам'яті вказаного ресурсу в мегабайтах.

### Список параметрів

`type`

Смотрите список[констант типів ресурсів](imagick.constants.md#imagick.constants.resourcetypes)

### Значення, що повертаються

Повертає розмір пам'яті вказаного ресурсу в мегабайтах.

### Помилки

Викликає ImagickException у разі виникнення помилки.
