---
navigation:
  - imagick.evaluateimage.md: '« Imagick::evaluateImage'
  - imagick.extentimage.md: 'Imagick::extentImage »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::exportImagePixels'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::exportImagePixels

(PECL imagick 2 >=2.3.0, PECL imagick 3)

Imagick::exportImagePixels — Експортує пікселі зображення

### Опис

```methodsynopsis
public Imagick::exportImagePixels(    int $x,    int $y,    int $width,    int $height,    string $map,    int $STORAGE): array
```

Експортує пікселі зображення до масиву. Параметр map визначає порядок експортованих пікселів. Розмір повертається масиву - `width * height * strlen(map)`. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.4.7 або старшим.

### Список параметрів

`x`

Координата X області, що експортується.

`y`

Координата Y області, що експортується.

`width`

Ширина області, що експортується.

`height`

Висота області, що експортується.

`map`

Порядок експортованих пікселів. Наприклад `"RGB"`. Допустимі символи для map: R, G, B, A, O, C, Y, M, K, I та P.

`STORAGE`

Зверніться до цього списку [констант типу PIXEL](imagick.constants.md#imagick.constants.pixel)

### Значення, що повертаються

Повертає масив, що містить значення пікселів.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** Imagick::exportImagePixels()\*\*\*\*

Експорт пікселів зображення в масив

```php
<?php

/* Создание нового объекта */
$im = new Imagick();

/* Создание нового изображения */
$im->newPseudoImage(0, 0, "magick:rose");

/* Экспорт пикселей изображения */
$pixels = $im->exportImagePixels(10, 10, 2, 2, "RGB", Imagick::PIXEL_CHAR);

/* Вывод */
var_dump($pixels);
?>
```

Результат виконання наведеного прикладу:

```
array(12) {
  [0]=>
  int(72)
  [1]=>
  int(64)
  [2]=>
  int(57)
  [3]=>
  int(69)
  [4]=>
  int(59)
  [5]=>
  int(43)
  [6]=>
  int(124)
  [7]=>
  int(120)
  [8]=>
  int(-96)
  [9]=>
  int(91)
  [10]=>
  int(84)
  [11]=>
  int(111)
}
```
