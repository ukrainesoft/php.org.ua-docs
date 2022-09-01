---
navigation:
  - imagickdraw.translate.html: '« ImagickDraw::translate'
  - imagickpixel.clear.html: 'ImagickPixel::clear »'
  - index.html: PHP Manual
  - book.imagick.html: ImageMagick
title: 'Клас [ImagickPixel](class.imagickpixel.html)'
---
# Клас [ImagickPixel](class.imagickpixel.html)

(PECL imagick 2, PECL imagick 3)

## Огляд класів

```classsynopsis

    
     class ImagickPixel
     {
    
   public clear(): bool
public __construct(string $color = ?)
public destroy(): bool
public getColor(int $normalized = 0): array
public getColorAsString(): string
public getColorCount(): int
public getColorQuantum(): array
public getColorValue(int $color): float
public getColorValueQuantum(int $color): int|float
public getHSL(): array
public getIndex(): int
public isPixelSimilar(ImagickPixel $color, float $fuzz): bool
public isPixelSimilarQuantum(string $color, string $fuzz = ?): bool
public isSimilar(ImagickPixel $color, float $fuzz): bool
public setColor(string $color): bool
public setcolorcount(int $colorCount): bool
public setColorValue(int $color, float $value): bool
public setColorValueQuantum(int $color, int|float $value): bool
public setHSL(float $hue, float $saturation, float $luminosity): bool
public setIndex(int $index): bool

   }
```

## Зміст

-   [ImagickPixel::clear](imagickpixel.clear.html) — Очищає ресурси, пов'язані із цим об'єктом
-   [ImagickPixel::construct](imagickpixel.construct.html) - Конструктор ImagickPixel
-   [ImagickPixel::destroy](imagickpixel.destroy.html) - Звільняє ресурси, пов'язані з цим об'єктом
-   [ImagickPixel::getColor](imagickpixel.getcolor.html) - Повертає колір
-   [ImagickPixel::getColorAsString](imagickpixel.getcolorasstring.html) — Повертає колір у вигляді рядка
-   [ImagickPixel::getColorCount](imagickpixel.getcolorcount.html) — Повертає кількість кольорів, пов'язаних із цим кольором.
-   [ImagickPixel::getColorQuantum](imagickpixel.getcolorquantum.html) - Опис
-   [ImagickPixel::getColorValue](imagickpixel.getcolorvalue.html) — Повертає нормалізоване значення кольору каналу
-   [ImagickPixel::getColorValueQuantum](imagickpixel.getcolorvaluequantum.html) - Опис
-   [ImagickPixel::getHSL](imagickpixel.gethsl.html) — Повертає нормалізований HSL-колір об'єкту ImagickPixel
-   [ImagickPixel::getIndex](imagickpixel.getindex.html) - Опис
-   [ImagickPixel::isPixelSimilar](imagickpixel.ispixelsimilar.html) — Перевіряє відстань між цим кольором та іншим
-   [ImagickPixel::isPixelSimilarQuantum](imagickpixel.ispixelsimilarquantum.html) - Опис
-   [ImagickPixel::isSimilar](imagickpixel.issimilar.html) — Перевірити різницю між цим кольором та іншим
-   [ImagickPixel::setColor](imagickpixel.setcolor.html) - Встановлює колір
-   [ImagickPixel::setColorCount](imagickpixel.setcolorcount.html) - Опис
-   [ImagickPixel::setColorValue](imagickpixel.setcolorvalue.html) - Встановлює нормалізоване значення одного з каналів
-   [ImagickPixel::setColorValueQuantum](imagickpixel.setcolorvaluequantum.html) - Опис
-   [ImagickPixel::setHSL](imagickpixel.sethsl.html) — Встановлення нормалізованого кольору HSL
-   [ImagickPixel::setIndex](imagickpixel.setindex.html) - Опис
