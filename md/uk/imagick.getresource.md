---
navigation:
  - imagick.getreleasedate.md: '« Imagick::getReleaseDate'
  - imagick.getresourcelimit.md: 'Imagick::getResourceLimit »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getResource'
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

Дивіться список [констант типов ресурсов](imagick.constants.md#imagick.constants.resourcetypes)

### Значення, що повертаються

Повертає розмір пам'яті вказаного ресурсу в мегабайтах.

### Помилки

Викликає ImagickException у разі виникнення помилки.
