---
navigation:
  - class.imagickpixeliterator.md: « ImagickPixelIterator
  - imagickpixeliterator.construct.md: 'ImagickPixelIterator::\_\_construct »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::clear'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixelIterator::clear

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::clear — Очищає ресурси, пов'язані з PixelIterator

### Опис

```methodsynopsis
public ImagickPixelIterator::clear(): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Очищає ресурси, пов'язані з PixelIterator.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** ImagickPixelIterator::clear()\*\*\*\*

```php
<?php
function clear($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));

    $imageIterator = $imagick->getPixelRegionIterator(100, 100, 250, 200);

    /* Походим по строкам пикселей */
    foreach ($imageIterator as $pixels) {
        /** @var $pixel \ImagickPixel */
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $column => $pixel) {
            if ($column % 2) {
                /* Красим каждый второй пиксель черным*/
                $pixel->setColor("rgba(0, 0, 0, 0)");
            }
        }
        /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
        $imageIterator->syncIterator();
    }

    $imageIterator->clear();

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```
