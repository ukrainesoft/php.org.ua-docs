Клас ImagickPixelIterator

-   [« ImagickPixel::setIndex](imagickpixel.setindex.html)
    
-   [ImagickPixelIterator::clear »](imagickpixeliterator.clear.html)
    
-   [PHP Manual](index.html)
    
-   [ImageMagick](book.imagick.html)
    
-   Клас ImagickPixelIterator
    

# Клас [ImagickPixelIterator](class.imagickpixeliterator.html)

(PECL imagick 2, PECL imagick 3)

## Огляд класів

```classsynopsis

    
     class ImagickPixelIterator
     {
    
   public clear(): bool
public __construct(Imagick $wand)
public destroy(): bool
public getCurrentIteratorRow(): array
public getIteratorRow(): int
public getNextIteratorRow(): array
public getPreviousIteratorRow(): array
public newPixelIterator(Imagick $wand): bool
public newPixelRegionIterator(    Imagick $wand,    int $x,    int $y,    int $columns,    int $rows): bool
public resetIterator(): bool
public setIteratorFirstRow(): bool
public setIteratorLastRow(): bool
public setIteratorRow(int $row): bool
public syncIterator(): bool

   }
```

## Зміст

-   [ImagickPixelIterator::clear](imagickpixeliterator.clear.html) — Очищає ресурси, пов'язані з PixelIterator
-   [ImagickPixelIterator::construct](imagickpixeliterator.construct.html) - Конструктор ImagickPixelIterator
-   [ImagickPixelIterator::destroy](imagickpixeliterator.destroy.html) — Звільняє ресурси, пов'язані з PixelIterator
-   [ImagickPixelIterator::getCurrentIteratorRow](imagickpixeliterator.getcurrentiteratorrow.html) — Повертає поточний ряд об'єкту ImagickPixel
-   [ImagickPixelIterator::getIteratorRow](imagickpixeliterator.getiteratorrow.html) - Повертає поточний піксель ітератора ряду
-   [ImagickPixelIterator::getNextIteratorRow](imagickpixeliterator.getnextiteratorrow.html) - Повертає наступний ряд ітератора пікселів
-   [ImagickPixelIterator::getPreviousIteratorRow](imagickpixeliterator.getpreviousiteratorrow.html) — Повертає попередній ряд
-   [ImagickPixelIterator::newPixelIterator](imagickpixeliterator.newpixeliterator.html) - Повертає новий ітератор пікселів
-   [ImagickPixelIterator::newPixelRegionIterator](imagickpixeliterator.newpixelregioniterator.html) - Повертає новий ітератор пікселів
-   [ImagickPixelIterator::resetIterator](imagickpixeliterator.resetiterator.html) — скидає ітератор пікселів
-   [ImagickPixelIterator::setIteratorFirstRow](imagickpixeliterator.setiteratorfirstrow.html) - Встановлює ітератор пікселів на перший ряд
-   [ImagickPixelIterator::setIteratorLastRow](imagickpixeliterator.setiteratorlastrow.html) - Встановлює ітератор пікселів на останній ряд
-   [ImagickPixelIterator::setIteratorRow](imagickpixeliterator.setiteratorrow.html) — Встановлює ряд в ітераторі пікселів
-   [ImagickPixelIterator::syncIterator](imagickpixeliterator.synciterator.html) - Синхронізує ітератор пікселів