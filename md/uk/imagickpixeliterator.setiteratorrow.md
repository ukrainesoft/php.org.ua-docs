---
navigation:
  - imagickpixeliterator.setiteratorlastrow.md: '« ImagickPixelIterator::setIteratorLastRow'
  - imagickpixeliterator.synciterator.md: 'ImagickPixelIterator::syncIterator »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::setIteratorRow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixelIterator::setIteratorRow

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::setIteratorRow - Встановлює номер ряду в ітераторі пікселів

### Опис

```methodsynopsis
public ImagickPixelIterator::setIteratorRow(int $row): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Встановлює ряд в ітераторі пікселів.

### Список параметрів

`row`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**ImagickPixelIterator::setIteratorRow()\*\*\*\*

```php
<?php
function setIteratorRow($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imageIterator = $imagick->getPixelRegionIterator(200, 100, 200, 200);

    for ($x = 0; $x < 20; $x++) {
        $imageIterator->setIteratorRow($x * 5);
        $pixels = $imageIterator->getCurrentIteratorRow();
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $pixel) {
            /** @var $pixel \ImagickPixel */
            /* Красим каждый второй пиксель черным*/
            $pixel->setColor("rgba(0, 0, 0, 0)");
        }

        /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
        $imageIterator->syncIterator();
    }

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```
