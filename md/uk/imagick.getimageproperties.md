---
navigation:
  - imagick.getimageprofiles.md: '« Imagick::getImageProfiles'
  - imagick.getimageproperty.md: 'Imagick::getImageProperty »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getImageProperties'
---
# Imagick::getImageProperties

(PECL imagick 2, PECL imagick 3)

Imagick::getImageProperties — Повертає властивості зображення

### Опис

```methodsynopsis
public Imagick::getImageProperties(string $pattern = "*", bool $include_values = true): array
```

Повертає всі властивості, що задовольняють шаблон. Якщо в якості другого параметра передано **`false`**, то повертаються лише назви властивостей. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.6 або старшим.

### Список параметрів

`pattern`

Шаблон для пошуку властивостей.

`include_values`

Повернути лише імена властивостей. Якщо передано **`false`**, то повертаються лише імена властивостей.

### Значення, що повертаються

Повертає масив, що містить властивості зображення чи їх імена.

### Приклади

**Приклад #1 Використання **Imagick::getImageProperties()****

Приклад отримання EXIF-інформації.

```php
<?php

/* Создание объекта */
$im = new imagick("/path/to/example.jpg");

/* Получение EXIF-информации */
$exifArray = $im->getImageProperties("exif:*");

/* Цикл по EXIF-свойствам */
foreach ($exifArray as $name => $property)
{
    echo "{$name} => {$property}<br />\n";
}

?>
```
