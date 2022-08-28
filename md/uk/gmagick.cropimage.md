Обрізає зображення

-   [« Gmagick::\_\_construct](gmagick.construct.html)
    
-   [Gmagick::cropthumbnailimage »](gmagick.cropthumbnailimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Обрізає зображення
    

# Gmagick::cropimage

(PECL gmagick >= Unknown)

Gmagick::cropimage — Обрізає зображення

### Опис

```methodsynopsis
public Gmagick::cropimage(    
    int
     $width
   ,    
    int
     $height
   ,    int $x,    int $y): Gmagick
```

Обрізає зображення.

### Список параметрів

`width`

Ширина ділянки, що зберігається.

`height`

Висота ділянки, що зберігається.

`x`

X координата лівого верхнього кута області, що зберігається.

`y`

Y координата лівого верхнього кута області, що зберігається.

### Значення, що повертаються

Обрізаний об'єкт [Gmagick](class.gmagick.html)

### Помилки

Викликає **GmagickException** у разі виникнення помилки.