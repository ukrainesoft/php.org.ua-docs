---
navigation:
  - imagick.setresolution.md: '« Imagick::setResolution'
  - imagick.setsamplingfactors.md: 'Imagick::setSamplingFactors »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setResourceLimit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setResourceLimit

(PECL imagick 2, PECL imagick 3)

Imagick::setResourceLimit — Встановлює ліміт для конкретного ресурсу

### Опис

```methodsynopsis
public static Imagick::setResourceLimit(int $type, int $limit): bool
```

Цей метод використовується для зміни ліміту ресурсів вихідної бібліотеки ImageMagick.

### Список параметрів

`type`

Обратитесь к списку[констант RESOURCETYPE](imagick.constants.md#imagick.constants.resourcetypes)

`limit`

Одна из[констант RESOURCETYPE](imagick.constants.md#imagick.constants.resourcetypes)Единица измерения зависит от типа ограничиваемого ресурса.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::getResourceLimit()](imagick.getresourcelimit.md) \- Повертає заданий ліміт ресурсів
