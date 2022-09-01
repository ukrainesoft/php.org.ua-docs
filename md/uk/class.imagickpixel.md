---
navigation:
  - imagickdraw.translate.html: '« ImagickDraw::translate'
  - imagickpixel.clear.html: 'ImagickPixel::clear »'
  - index.html: PHP Manual
  - book.imagick.html: ImageMagick
title: 'Клас [ImagickPixel](class.imagickpixel.md)'
---
# Клас [ImagickPixel](class.imagickpixel.md)

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

-   [ImagickPixel::clear](imagickpixel.clear.md) — Очищає ресурси, пов'язані із цим об'єктом
-   [ImagickPixel::construct](imagickpixel.construct.md) - Конструктор ImagickPixel
-   [ImagickPixel::destroy](imagickpixel.destroy.md) - Звільняє ресурси, пов'язані з цим об'єктом
-   [ImagickPixel::getColor](imagickpixel.getcolor.md) - Повертає колір
-   [ImagickPixel::getColorAsString](imagickpixel.getcolorasstring.md) — Повертає колір у вигляді рядка
-   [ImagickPixel::getColorCount](imagickpixel.getcolorcount.md) — Повертає кількість кольорів, пов'язаних із цим кольором.
-   [ImagickPixel::getColorQuantum](imagickpixel.getcolorquantum.md) - Опис
-   [ImagickPixel::getColorValue](imagickpixel.getcolorvalue.md) — Повертає нормалізоване значення кольору каналу
-   [ImagickPixel::getColorValueQuantum](imagickpixel.getcolorvaluequantum.md) - Опис
-   [ImagickPixel::getHSL](imagickpixel.gethsl.md) — Повертає нормалізований HSL-колір об'єкту ImagickPixel
-   [ImagickPixel::getIndex](imagickpixel.getindex.md) - Опис
-   [ImagickPixel::isPixelSimilar](imagickpixel.ispixelsimilar.md) — Перевіряє відстань між цим кольором та іншим
-   [ImagickPixel::isPixelSimilarQuantum](imagickpixel.ispixelsimilarquantum.md) - Опис
-   [ImagickPixel::isSimilar](imagickpixel.issimilar.md) — Перевірити різницю між цим кольором та іншим
-   [ImagickPixel::setColor](imagickpixel.setcolor.md) - Встановлює колір
-   [ImagickPixel::setColorCount](imagickpixel.setcolorcount.md) - Опис
-   [ImagickPixel::setColorValue](imagickpixel.setcolorvalue.md) - Встановлює нормалізоване значення одного з каналів
-   [ImagickPixel::setColorValueQuantum](imagickpixel.setcolorvaluequantum.md) - Опис
-   [ImagickPixel::setHSL](imagickpixel.sethsl.md) — Встановлення нормалізованого кольору HSL
-   [ImagickPixel::setIndex](imagickpixel.setindex.md) - Опис
