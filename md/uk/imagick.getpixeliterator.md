---
navigation:
  - imagick.getpage.md: '« Imagick::getPage'
  - imagick.getpixelregioniterator.md: 'Imagick::getPixelRegionIterator »'
  - index.md: PHP Manual
  - class.imagick.md: Imagick
title: 'Imagick::getPixelIterator'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Imagick::getPixelIterator

(PECL imagick 2, PECL imagick 3)

Imagick::getPixelIterator — Повертає MagickPixelIterator

### Опис

```methodsynopsis
public Imagick::getPixelIterator(): ImagickPixelIterator
```

Повертає MagickPixelIterator.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ImagickPixelIterator у разі успішного виконання.

### Помилки

Викликає ImagickException у разі виникнення помилки.

### Приклади

**Пример #1 Пример использования**Imagick::getPixelIterator()\*\*\*\*

```php
<?php
function getPixelIterator($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imageIterator = $imagick->getPixelIterator();

    foreach ($imageIterator as $row => $pixels) { /* Проход по строкам пикселей в цикле */
        foreach ($pixels as $column => $pixel) { /* Проход по пикселям в строке (по столбцам) */
            /** @var $pixel \ImagickPixel */
            if ($column % 2) {
                $pixel->setColor("rgba(0, 0, 0, 0)"); /* Закрашивание каждого второго пикселя в черный цвет */
            }
        }
        $imageIterator->syncIterator(); /* Синхронизация итератора, это важно делать на каждой итерации. */
    }

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```
