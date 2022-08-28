Витягує область зображення

-   [« Imagick::getImageRedPrimary](imagick.getimageredprimary.html)
    
-   [Imagick::getImageRenderingIntent »](imagick.getimagerenderingintent.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Витягує область зображення
    

# Imagick::getImageRegion

(PECL imagick 2, PECL imagick 3)

Imagick::getImageRegion — Витягує область зображення

### Опис

```methodsynopsis
public Imagick::getImageRegion(    int $width,    int $height,    int $x,    int $y): Imagick
```

Витягує область зображення та повертає її у вигляді нового об'єкта Imagick.

### Список параметрів

`width`

Ширина вилученої області.

`height`

Висота витягнутої області.

`x`

Координата X лівого верхнього кута одержаної області.

`y`

Координата Y лівого верхнього кута одержаної області.

### Значення, що повертаються

Витягує область зображення та повертає її у вигляді нової палички.

### Помилки

Викликає ImagickException у разі виникнення помилки.