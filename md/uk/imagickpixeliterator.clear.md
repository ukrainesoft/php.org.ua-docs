Очищає ресурси, пов'язані з PixelIterator

-   [« ImagickPixelIterator](class.imagickpixeliterator.html)
    
-   [ImagickPixelIterator::construct »](imagickpixeliterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixelIterator](class.imagickpixeliterator.html)
    
-   Очищає ресурси, пов'язані з PixelIterator
    

# ImagickPixelIterator::clear

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::clear — Очищає ресурси, пов'язані з PixelIterator

### Опис

```methodsynopsis
public ImagickPixelIterator::clear(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Очищає ресурси, пов'язані з PixelIterator.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickPixelIterator::clear()****

```php
<?php
function clear($imagePath) {
    $imagick = new \Imagick(realpath($imagePath));

    $imageIterator = $imagick->getPixelRegionIterator(100, 100, 250, 200);

    /* Походим по строкам пикселей */
    foreach ($imageIterator as $pixels) {
        /** @var $pixel \ImagickPixel */
        /* Походим по пикселям в строке (столбцы) */
        foreach ($pixels as $column => $pixel) {
            if ($column % 2) {
                /* Красим каждый второй пиксель черным*/
                $pixel->setColor("rgba(0, 0, 0, 0)");
            }
        }
        /* Синхронизируем итератор. Это необходимо для делать на каждой итерации */
        $imageIterator->syncIterator();
    }

    $imageIterator->clear();

    header("Content-Type: image/jpg");
    echo $imagick;
}

?>
```