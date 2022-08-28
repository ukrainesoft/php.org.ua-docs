Повертає наступний ряд ітератора пікселів

-   [« ImagickPixelIterator::getIteratorRow](imagickpixeliterator.getiteratorrow.html)
    
-   [ImagickPixelIterator::getPreviousIteratorRow »](imagickpixeliterator.getpreviousiteratorrow.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixelIterator](class.imagickpixeliterator.html)
    
-   Повертає наступний ряд ітератора пікселів
    

# ImagickPixel Iterator::getNext Iterator Row

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::getNextIteratorRow - Повертає наступний ряд ітератора пікселів

### Опис

```methodsynopsis
public ImagickPixelIterator::getNextIteratorRow(): array
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає наступний ряд як масиву пікселів з ітератора пікселів.

### Значення, що повертаються

Повертає наступний ряд у вигляді масиву об'єктів ImagickPixel, у разі виникнення помилки видасть виняток ImagickPixelIteratorException.

### Приклади

**Приклад #1 Приклад використання **ImagickPixel Iterator::getNext Iterator Row()****

```php
<?php
function getNextIteratorRow($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));
    $imageIterator = $imagick->getPixelIterator();

    $count = 0;
    while ($pixels = $imageIterator->getNextIteratorRow()) {
        if (($count % 3) == 0) {
            /* Походим по пикселям в строке (столбцы) */
            foreach ($pixels as $column => $pixel) {
                /** @var $pixel \ImagickPixel */
                if ($column % 2) {
                    /* Красим каждый второй пиксель черным*/
                    $pixel->setColor("rgba(0, 0, 0, 0)");
                }
            }
            /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
            $imageIterator->syncIterator();
        }

        $count += 1;
    }

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```