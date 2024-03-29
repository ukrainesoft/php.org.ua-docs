---
navigation:
  - imagick.negateimage.md: '« Imagick::negateImage'
  - imagick.newpseudoimage.md: 'Imagick::newPseudoImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::newImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::newImage

(PECL imagick 2, PECL imagick 3)

Imagick::newImage — Створює нове зображення

### Опис

```methodsynopsis
public Imagick::newImage(    int $cols,    int $rows,    mixed $background,    string $format = ?): bool
```

Створює нове зображення і пов'язує значення ImagickPixel як колір тла

### Список параметрів

`cols`

Стовпці у новому зображенні

`rows`

Рядки у новому зображенні

`background`

Колір фону для цього зображення

`format`

Формат зображення. Цей параметр був доданий до Imagick версії 2.0.1.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Тепер допускається рядок, що представляє колір, як третій параметр. Раніше допускався лише об'єкт ImagickPixel. |

### Приклади

**Приклад #1 Приклад використання** Imagick::newImage()\*\* :\*\*

Створення нового зображення та його відображення.

```php
<?php

$image = new Imagick();
$image->newImage(100, 100, new ImagickPixel('red'));
$image->setImageFormat('png');

header('Content-type: image/png');
echo $image;

?>
```
