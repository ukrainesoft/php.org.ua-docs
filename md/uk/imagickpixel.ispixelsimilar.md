---
navigation:
  - imagickpixel.getindex.md: '« ImagickPixel::getIndex'
  - imagickpixel.ispixelsimilarquantum.md: 'ImagickPixel::isPixelSimilarQuantum »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::isPixelSimilar'
---
# ImagickPixel::isPixelSimilar

(PECL imagick 3> = 3.3.0)

ImagickPixel::isPixelSimilar — Перевіряє відстань між цим кольором та іншим

### Опис

```methodsynopsis
public ImagickPixel::isPixelSimilar(ImagickPixel $color, float $fuzz): bool
```

Перевіряє відстань між кольором, описаним цим об'єктом ImagickPixel, та кольором наданого об'єкта, наносячи їх значення RGB на кольоровий куб. Якщо відстань між двома точками менша за задане значення розмиття, кольори схожі. Метод замінює [ImagickPixel::isSimilar()](imagickpixel.issimilar.md) і коректно нормалізує значення fuzz у ImageMagick QuantumRange.

### Список параметрів

`color`

Об'єкт ImagickPixel можна порівняти з поточним об'єктом.

`fuzz`

Максимальна відстань, на якій можна вважати ці кольори однаковими. Теоретичним максимумом для цього значення є квадратний корінь із трьох (1,732).

### Значення, що повертаються

У разі успішної роботи повертає **`true`**
