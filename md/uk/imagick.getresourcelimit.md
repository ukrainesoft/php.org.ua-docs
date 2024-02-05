---
navigation:
  - imagick.getresource.md: '« Imagick::getResource'
  - imagick.getsamplingfactors.md: 'Imagick::getSamplingFactors »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getResourceLimit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getResourceLimit

(PECL imagick 2, PECL imagick 3)

Imagick::getResourceLimit — Повертає заданий ліміт ресурсів

### Опис

```methodsynopsis
public static Imagick::getResourceLimit(int $type): int
```

Повертає заданий ліміт ресурсів.

### Список параметрів

`type`

Одна из[констант типів ресурсів](imagick.constants.md#imagick.constants.resourcetypes)Блок (unit) зависит от типа ограниченного ресурса.

### Значення, що повертаються

Повертає заданий ліміт ресурсів у мегабайтах.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Дивіться також

-   [Imagick::setResourceLimit()](imagick.setresourcelimit.md) \- встановлює ліміт для конкретного ресурсу
