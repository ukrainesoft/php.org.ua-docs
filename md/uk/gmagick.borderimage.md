Додати рамку до зображення

-   [« Gmagick::blurimage](gmagick.blurimage.html)
    
-   [Gmagick::charcoalimage »](gmagick.charcoalimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Додати рамку до зображення
    

# Gmagick::borderimage

(PECL gmagick >= Unknown)

Gmagick::borderimage — Додати рамку до зображення

### Опис

```methodsynopsis
public Gmagick::borderimage(GmagickPixel $color, int $width, int $height): Gmagick
```

Додати рамку зображення. Колір рамки задається рядком або кольором фону об'єкта [GmagickPixel](class.gmagickpixel.html)

### Список параметрів

`color`

Об'єкт [GmagickPixel](class.gmagickpixel.html) object або рядок, що визначає колір рамки.

`width`

Товщина кадру.

`height`

Висота кадру.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) з доданою рамкою.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.