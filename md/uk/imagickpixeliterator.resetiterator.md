Скидає ітератор пікселів

-   [« ImagickPixelIterator::newPixelRegionIterator](imagickpixeliterator.newpixelregioniterator.html)
    
-   [ImagickPixelIterator::setIteratorFirstRow »](imagickpixeliterator.setiteratorfirstrow.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixelIterator](class.imagickpixeliterator.html)
    
-   Скидає ітератор пікселів
    

# ImagickPixel Iterator::reset Iterator

(PECL imagick 2, PECL imagick 3)

ImagickPixel Iterator::reset Iterator — Скидає ітератор пікселів

### Опис

```methodsynopsis
public ImagickPixelIterator::resetIterator(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Скидає ітератор пікселів. Використовуйте разом із ImagickPixelIterator::getNextIteratorRow() для перебору всіх пікселів у контейнері пікселів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickPixel Iterator::reset Iterator()****

```php
<?php
function resetIterator($imagePath) {

    $imagick = new \Imagick(realpath($imagePath));

    $imageIterator = $imagick->getPixelIterator();

    /* Походим по строкам пикселей */
    foreach ($imageIterator as $pixels) {
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $column => $pixel) {
            /** @var $pixel \ImagickPixel */
            if ($column % 2) {

                /* Делаем каждый второй пиксель на 25% красным*/
                $pixel->setColorValue(\Imagick::COLOR_RED, 64);
            }
        }
        /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
        $imageIterator->syncIterator();
    }

    $imageIterator->resetiterator();

    /* Походим по строкам пикселей */
    foreach ($imageIterator as $pixels) {
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $column => $pixel) {
            /** @var $pixel \ImagickPixel */
            if ($column % 3) {
                $pixel->setColorValue(\Imagick::COLOR_BLUE, 64); /* Делаем каждый второй пиксель немного синим*/
                //$pixel->setColor("rgba(0, 0, 128, 0)"); /* Paint every second pixel black*/
            }
        }
        $imageIterator->syncIterator(); /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
    }

    $imageIterator->clear();

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```