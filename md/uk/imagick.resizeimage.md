---
navigation:
  - imagick.resetimagepage.md: '« Imagick::resetImagePage'
  - imagick.rollimage.md: 'Imagick::rollImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::resizeImage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::resizeImage

(PECL imagick 2, PECL imagick 3)

Imagick::resizeImage — Масштабування зображення

### Опис

```methodsynopsis
public Imagick::resizeImage(    int $columns,    int $rows,    int $filter,    float $blur,    bool $bestfit = false,    bool $legacy = false): bool
```

Масштабує зображення до бажаних розмірів за допомогою [filter](imagick.constants.md#imagick.constants.filters)

> **Зауваження**: Поведение параметра`bestfit` було змінено у Imagick 3.0.0. До цієї версії при зміні зображення розміром 200 x 150 до 400 x 300 жодних операцій не відбувалося. В Imagick 3.0.0 і пізніших версіях зображення буде масштабовано до розміру 400 x 300, тому що найбільше відповідає ("best fit") даним розмірам. Якщо вказано параметр `bestfit`, то ширина та висота також повинні бути визначені.

### Список параметрів

`columns`

Ширина зображення.

`rows`

Висота зображення.

`filter`

Обратитесь к списку[констант FILTER](imagick.constants.md#imagick.constants.filters)

`blur`

Коефіцієнт розмиття, де значення > 1 робить зображення більш розмитим, а значення < 1 - різкішим.

`bestfit`

Необов'язковий параметр припасування.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL imagick 2.1.0 | Додано необов'язковий параметр припасування. Тепер метод підтримує пропорційне масштабування. Для пропорційного масштабування необхідно передати нуль як будь-який параметр. |

### Приклади

**Приклад #1 Приклад використання** Imagick::resizeImage()\*\*\*\*

```php
<?php
function resizeImage($imagePath, $width, $height, $filterType, $blur, $bestFit, $cropZoom) {
    //Коэффициент размытия, где значение >  1 делает изображение более размытым, а значение < 1 - более резким.
    $imagick = new \Imagick(realpath($imagePath));

    $imagick->resizeImage($width, $height, $filterType, $blur, $bestFit);

    $cropWidth = $imagick->getImageWidth();
    $cropHeight = $imagick->getImageHeight();

    if ($cropZoom) {
        $newWidth = $cropWidth / 2;
        $newHeight = $cropHeight / 2;

        $imagick->cropimage(
            $newWidth,
            $newHeight,
            ($cropWidth - $newWidth) / 2,
            ($cropHeight - $newHeight) / 2
        );

        $imagick->scaleimage(
            $imagick->getImageWidth() * 4,
            $imagick->getImageHeight() * 4
        );
    }


    header("Content-Type: image/jpg");
    echo $imagick->getImageBlob();
}

?>
```
