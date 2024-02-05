---
navigation:
  - gmagickdraw.settextencoding.md: '« GmagickDraw::settextencoding'
  - gmagickpixel.construct.md: 'GmagickPixel::\_\_construct »'
  - index.md: PHP Manual
  - book.gmagick.md: Gmagick
title: Клас GmagickPixel
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас GmagickPixel

(PECL gmagick >= Unknown)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class GmagickPixel
     
     {
    

    /* Методы */
    
   public __construct(string $color = ?)

    public getcolor(bool $as_array = false, bool $normalize_array = false): mixed
public getcolorcount(): int
public getcolorvalue(int $color): float
public setcolor(string $color): GmagickPixel
public setcolorvalue(int $color, float $value): GmagickPixel

   }
```

## Зміст

-   [GmagickPixel::\_\_construct](gmagickpixel.construct.md) \- Конструктора класу GmagickPixel
-   [GmagickPixel::getcolor](gmagickpixel.getcolor.md) \- Повертає колір
-   [GmagickPixel::getcolorcount](gmagickpixel.getcolorcount.md)— Отримати кількість пікселів зображення, які мають заданий колір
-   [GmagickPixel::getcolorvalue](gmagickpixel.getcolorvalue.md)— Повертає нормалізоване значення для заданого каналу кольорів
-   [GmagickPixel::setcolor](gmagickpixel.setcolor.md) \- Задати колір
-   [GmagickPixel::setcolorvalue](gmagickpixel.setcolorvalue.md)— Встановити нормалізоване значення колірного каналу
