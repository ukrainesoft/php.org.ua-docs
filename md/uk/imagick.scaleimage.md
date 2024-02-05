---
navigation:
  - imagick.sampleimage.md: '« Imagick::sampleImage'
  - imagick.segmentimage.md: 'Imagick::segmentImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::scaleImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::scaleImage

(PECL imagick 2, PECL imagick 3)

Imagick::scaleImage — Масштабує розмір зображення

### Опис

```methodsynopsis
public Imagick::scaleImage(    int $columns,    int $rows,    bool $bestfit = false,    bool $legacy = false): bool
```

Масштабує зображення до розмірів. Другий параметр буде обчислено, якщо в якості будь-якого з параметрів буде передано 0.

> **Зауваження**: Поведение параметра`bestfit` було змінено у Imagick 3.0.0. До цієї версії при зміні зображення розміром 200 x 150 до 400 x 300 жодних операцій не відбувалося. В Imagick 3.0.0 і пізніших версіях зображення буде масштабовано до розміру 400 x 300, тому що найбільше відповідає ("best fit") даним розмірам. Якщо вказано параметр `bestfit`, то ширина та висота також повинні бути визначені.

### Список параметрів

`columns`

`rows`

`bestfit`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Помилки

Викликає ImagickException у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Доданий необов'язковий параметр fit. Метод тепер підтримує пропорційне масштабування. Передайте нуль як будь-який параметр для пропорційного масштабування. |

### Приклади

**Пример #1 Пример использования**Imagick::scaleImage()\*\*\*\*

```php
<?php
function scaleImage($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imagick->scaleImage(150, 150, true);
    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
