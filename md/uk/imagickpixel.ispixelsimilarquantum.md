---
navigation:
  - imagickpixel.ispixelsimilar.md: '« ImagickPixel::isPixelSimilar'
  - imagickpixel.issimilar.md: 'ImagickPixel::isSimilar »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::isPixelSimilarQuantum'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::isPixelSimilarQuantum

(PECL imagick 3 >= 3.3.0)

ImagickPixel::isPixelSimilarQuantum — Повертає true, якщо відстань між двома кольорами менша від зазначеної відстані

### Опис

```methodsynopsis
public ImagickPixel::isPixelSimilarQuantum(string $color, string $fuzz = ?): bool
```

Повертає true, якщо відстань між двома кольорами менша від зазначеної відстані. Значення fuzz має бути в діапазоні від 0 до QuantumRange. Максимальне значення становить максимально можливу відстань у колірному просторі. Наприклад, від RGB (0, 0, 0) до RGB (255, 255, 255) для колірного простору RGB

### Список параметрів

`color`

`fuzz`

### Значення, що повертаються
