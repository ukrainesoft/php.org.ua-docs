---
navigation:
  - imagickpixeliterator.clear.md: '« ImagickPixelIterator::clear'
  - imagickpixeliterator.destroy.md: 'ImagickPixelIterator::destroy »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::construct'
---
# ImagickPixelIterator::construct

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::construct — Конструктор ImagickPixelIterator

### Опис

```methodsynopsis
public ImagickPixelIterator::__construct(Imagick $wand)
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Конструктор ImagickPixelIterator

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickPixelIterator::construct()****

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
