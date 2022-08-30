Додає змодельований тривимірний кордон

-   [« Gmagick::flopimage](gmagick.flopimage.md)
    
-   [Gmagick::gammaimage »](gmagick.gammaimage.md)
    
-   [PHP Manual](index.md)
    
-   [Gmagick](class.gmagick.md)
    
-   Додає змодельований тривимірний кордон
    

# Gmagick::frameimage

(PECL gmagick >= Unknown)

Gmagick::frameimage — Додає змодельований тривимірний кордон

### Опис

```methodsynopsis
public Gmagick::frameimage(    GmagickPixel $color,    int $width,    int $height,    int $inner_bevel,    int $outer_bevel): Gmagick
```

Додає змодельовану тривимірну рамку навколо зображення. Ширина та висота визначають ширину межі вертикальної та горизонтальної сторін рамки. Внутрішній та зовнішній скоси вказують ширину внутрішньої та зовнішньої тіней рамки.

### Список параметрів

`color`

Об'єкт [GmagickPixel](class.gmagickpixel.md) або число з плаваючою точкою, що представляє матовий колір.

`width`

Ширина кордону.

`height`

Висота кордону.

`inner_bevel`

Внутрішня ширина скосу.

`outer_bevel`

Зовнішня ширина скосу.

### Значення, що повертаються

Обрамлений об'єкт [Gmagick](class.gmagick.md)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.