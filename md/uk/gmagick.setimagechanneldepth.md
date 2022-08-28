Встановлює глибину певного каналу зображення

-   [« Gmagick::setimagebordercolor](gmagick.setimagebordercolor.html)
    
-   [Gmagick::setimagecolorspace »](gmagick.setimagecolorspace.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Встановлює глибину певного каналу зображення
    

# Gmagick::setimagechanneldepth

(PECL gmagick >= Unknown)

Gmagick::setimagechanneldepth — Встановлює глибину певного каналу зображення

### Опис

```methodsynopsis
public Gmagick::setimagechanneldepth(int $channel, int $depth): Gmagick
```

Встановлює глибину певного каналу зображення.

### Список параметрів

`channel`

Одна з констант [канала](gmagick.constants.html#gmagick.constants.channel) `Gmagick::CHANNEL_*`

`depth`

Глибина зображення у бітах.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.