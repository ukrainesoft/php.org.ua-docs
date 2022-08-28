Створює нове зображення

-   [« Gmagick::motionblurimage](gmagick.motionblurimage.html)
    
-   [Gmagick::nextimage »](gmagick.nextimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Створює нове зображення
    

# Gmagick::newimage

(PECL gmagick >= Unknown)

Gmagick::newimage — Створює нове зображення

### Опис

```methodsynopsis
public Gmagick::newimage(    int $width,    int $height,    string $background,    string $format = ?): Gmagick
```

Створює нове зображення із зазначеним фоновим кольором.

### Список параметрів

`width`

Ширина нового зображення.

`height`

Висота нового зображення.

`background`

Колір фону, який використовується для цього зображення у вигляді числа з плаваючою точкою.

`format`

Формат зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.