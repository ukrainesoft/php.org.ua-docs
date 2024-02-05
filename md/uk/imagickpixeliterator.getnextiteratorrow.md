---
navigation:
  - imagickpixeliterator.getiteratorrow.md: '« ImagickPixelIterator::getIteratorRow'
  - imagickpixeliterator.getpreviousiteratorrow.md: 'ImagickPixelIterator::getPreviousIteratorRow »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::getNextIteratorRow'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixelIterator::getNextIteratorRow

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::getNextIteratorRow - Повертає наступний ряд ітератора пікселів

### Опис

```methodsynopsis
public ImagickPixelIterator::getNextIteratorRow(): array
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Повертає наступний ряд як масиву пікселів з ітератора пікселів.

### Значення, що повертаються

Повертає наступний ряд у вигляді масиву об'єктів ImagickPixel, у разі виникнення помилки видасть виняток ImagickPixelIteratorException.

### Приклади

**Пример #1 Пример использования**ImagickPixelIterator::getNextIteratorRow()\*\*\*\*

```php
<?php
function getNextIteratorRow($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imageIterator = $imagick->getPixelIterator();

    $count = 0;
    while ($pixels = $imageIterator->getNextIteratorRow()) {
        if (($count % 3) == 0) {
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

        $count += 1;
    }

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```
