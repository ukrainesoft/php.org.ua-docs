---
navigation:
  - imagickpixel.setindex.md: '« ImagickPixel::setIndex'
  - imagickpixeliterator.clear.md: 'ImagickPixelIterator::clear »'
  - index.md: PHP Manual
  - book.imagick.md: ImageMagick
title: 'Клас ImagickPixelIterator'
---
# Клас [ImagickPixelIterator](class.imagickpixeliterator.md)

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

-   [ImagickPixelIterator::clear](imagickpixeliterator.clear.md) — Очищає ресурси, пов'язані з PixelIterator
-   [ImagickPixelIterator::construct](imagickpixeliterator.construct.md) - Конструктор ImagickPixelIterator
-   [ImagickPixelIterator::destroy](imagickpixeliterator.destroy.md) — Звільняє ресурси, пов'язані з PixelIterator
-   [ImagickPixelIterator::getCurrentIteratorRow](imagickpixeliterator.getcurrentiteratorrow.md) — Повертає поточний ряд об'єкту ImagickPixel
-   [ImagickPixelIterator::getIteratorRow](imagickpixeliterator.getiteratorrow.md) - Повертає поточний піксель ітератора ряду
-   [ImagickPixelIterator::getNextIteratorRow](imagickpixeliterator.getnextiteratorrow.md) - Повертає наступний ряд ітератора пікселів
-   [ImagickPixelIterator::getPreviousIteratorRow](imagickpixeliterator.getpreviousiteratorrow.md) — Повертає попередній ряд
-   [ImagickPixelIterator::newPixelIterator](imagickpixeliterator.newpixeliterator.md) - Повертає новий ітератор пікселів
-   [ImagickPixelIterator::newPixelRegionIterator](imagickpixeliterator.newpixelregioniterator.md) - Повертає новий ітератор пікселів
-   [ImagickPixelIterator::resetIterator](imagickpixeliterator.resetiterator.md) — скидає ітератор пікселів
-   [ImagickPixelIterator::setIteratorFirstRow](imagickpixeliterator.setiteratorfirstrow.md) - Встановлює ітератор пікселів на перший ряд
-   [ImagickPixelIterator::setIteratorLastRow](imagickpixeliterator.setiteratorlastrow.md) - Встановлює ітератор пікселів на останній ряд
-   [ImagickPixelIterator::setIteratorRow](imagickpixeliterator.setiteratorrow.md) — Встановлює ряд в ітераторі пікселів
-   [ImagickPixelIterator::syncIterator](imagickpixeliterator.synciterator.md) - Синхронізує ітератор пікселів
