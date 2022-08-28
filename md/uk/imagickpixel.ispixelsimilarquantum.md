Опис

-   [« ImagickPixel::isPixelSimilar](imagickpixel.ispixelsimilar.html)
    
-   [ImagickPixel::isSimilar »](imagickpixel.issimilar.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickPixel](class.imagickpixel.html)
    
-   Опис
    

# ImagickPixel::isPixelSimilarQuantum

(PECL imagick 3> = 3.3.0)

ImagickPixel::isPixelSimilarQuantum — Опис

### Опис

```methodsynopsis
public ImagickPixel::isPixelSimilarQuantum(string $color, string $fuzz = ?): bool
```

Повертає true, якщо відстань між двома кольорами менша за вказану відстань. Значення fuzz має бути в діапазоні від 0 до QuantumRange. Максимальне значення становить максимально можливу відстань у колірному просторі. Наприклад, від RGB (0, 0, 0) до RGB (255, 255, 255) для колірного простору RGB

### Список параметрів

`color`

`fuzz`

### Значення, що повертаються