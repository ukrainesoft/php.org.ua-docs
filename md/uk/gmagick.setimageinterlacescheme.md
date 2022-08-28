Встановлює схему надстрокової розгортки зображення

-   [« Gmagick::setimageindex](gmagick.setimageindex.html)
    
-   [Gmagick::setimageiterations »](gmagick.setimageiterations.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Встановлює схему надстрокової розгортки зображення
    

# Gmagick::setimageinterlacescheme

(PECL gmagick >= Unknown)

Gmagick::setimageinterlacescheme — Встановлює схему надстрокової розгортки зображення

### Опис

```methodsynopsis
public Gmagick::setimageinterlacescheme(int $interlace): Gmagick
```

Встановлює схему черезрядкової розгортки зображення.

### Список параметрів

`interlace`

Одна з констант [схемы чересстрочного изображения](gmagick.constants.html#gmagick.constants.interlace) `Gmagick::INTERLACE_*`

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.