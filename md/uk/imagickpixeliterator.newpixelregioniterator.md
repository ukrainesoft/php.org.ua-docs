---
navigation:
  - imagickpixeliterator.newpixeliterator.md: '« ImagickPixelIterator::newPixelIterator'
  - imagickpixeliterator.resetiterator.md: 'ImagickPixelIterator::resetIterator »'
  - index.md: PHP Manual
  - class.imagickpixeliterator.md: ImagickPixelIterator
title: 'ImagickPixelIterator::newPixelRegionIterator'
---
# ImagickPixelIterator::newPixelRegionIterator

(PECL imagick 2, PECL imagick 3)

ImagickPixelIterator::newPixelRegionIterator — Повертає новий ітератор пікселів

### Опис

```methodsynopsis
public ImagickPixelIterator::newPixelRegionIterator(    Imagick $wand,    int $x,    int $y,    int $columns,    int $rows): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Повертає новий ітератор пікселів.

### Список параметрів

`wand`

`x`

`y`

`columns`

`rows`

### Значення, що повертаються

Повертає новий об'єкт ImagickPixelIterator у разі успішного виконання; в іншому випадку викидає виняток ImagickPixelIteratorException.
