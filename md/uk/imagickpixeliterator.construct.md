---
navigation:
  - imagickpixeliterator.clear.md: '« ImagickPixelIterator::clear'
  - imagickpixeliterator.destroy.md: 'ImagickPixelIterator::destroy »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixelIterator::\_\_construct

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::\_\_construct — Конструктор ImagickPixelIterator

### Опис

```methodsynopsis
public ImagickPixelIterator::__construct(Imagick $wand)
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Конструктор ImagickPixelIterator

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** ImagickPixelIterator::construct()\*\*\*\*

```php
<?php
function construct($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imageIterator = new \ImagickPixelIterator($imagick);

    /* Походим по строкам пикселей */
    foreach ($imageIterator as $pixels) {
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $column => $pixel) {
            /** @var $pixel \ImagickPixel */
            if ($column % 2) {
                /* Красим каждый второй пиксель черным*/
                $pixel->setColor("rgba(0, 0, 0, 0)");
            }
        }
        /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
        $imageIterator->syncIterator();
    }

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```
