---
navigation:
  - imagick.setprogressmonitor.md: '« Imagick::setProgressMonitor'
  - imagick.setresolution.md: 'Imagick::setResolution »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::setRegistry'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::setRegistry

(PECL imagick 3 >= 3.3.0)

Imagick::setRegistry — Встановлює значення для запису реєстру ImageMagick з ім'ям key

### Опис

```methodsynopsis
public static Imagick::setRegistry(string $key, string $value): bool
```

Встановлює значення запису реєстру ImageMagick з ім'ям key. Найкорисніше для встановлення тимчасового шляху, який визначає, де ImageMagick створює тимчасові зображення, наприклад, при обробці PDF-файлів.

### Список параметрів

`key`

`value`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
