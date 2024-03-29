---
navigation:
  - imagick.getpixeliterator.md: '« Imagick::getPixelIterator'
  - imagick.getpointsize.md: 'Imagick::getPointSize »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getPixelRegionIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getPixelRegionIterator

(PECL imagick 2, PECL imagick 3)

Imagick::getPixelRegionIterator — Повертає об'єкт ImagickPixelIterator для розділу зображення

### Опис

```methodsynopsis
public Imagick::getPixelRegionIterator(    int $x,    int $y,    int $columns,    int $rows): ImagickPixelIterator
```

Повертає об'єкт ImagickPixelIterator для секції зображення.

### Список параметрів

`x`

Координати області X.

`y`

Координати області Y.

`columns`

Ширина області.

`rows`

Висота області.

### Значення, що повертаються

Повертає об'єкт ImagickPixelIterator для секції зображення.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання функції** Imagick::getPixelRegionIterator()\*\*\*\*

Пробігає пікселями вгорі зліва зображення і замінює їх на чорні.

```php
<?php
$im = new Imagick(realpath("./testImage.png"));
$areaIterator = $im->getPixelRegionIterator(0, 0, 10, 10);

foreach ($areaIterator as $rowIterator) {
    foreach ($rowIterator as $pixel) {
        // Красит каждый пиксель черным
        $pixel->setColor("rgba(0, 0, 0, 0)");
    }
    $areaIterator->syncIterator();
}
$im->writeImage("./output.png");
?>
```
