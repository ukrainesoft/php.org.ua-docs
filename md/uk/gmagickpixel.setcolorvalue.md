Встановити нормалізоване значення колірного каналу

-   [« GmagickPixel::setcolor](gmagickpixel.setcolor.html)
    
-   [ImageMagick »](book.imagick.html)
    
-   [PHP Manual](index.html)
    
-   [GmagickPixel](class.gmagickpixel.html)
    
-   Встановити нормалізоване значення колірного каналу
    

# GmagickPixel::setcolorvalue

(PECL gmagick >= Unknown)

GmagickPixel::setcolorvalue — Встановити нормалізоване значення колірного каналу

### Опис

```methodsynopsis
public GmagickPixel::setcolorvalue(int $color, float $value): GmagickPixel
```

Встановлює нормалізоване значення колірного каналу. Значення має бути числом з плаваючою точкою (float) у діапазоні від 0 до 1. Також ця функція може використовуватись для завдання каналу прозорості об'єкта [GmagickPixel](class.gmagickpixel.html)

### Список параметрів

`color`

Колірний канал. Одна із констант колірних каналів Gmagick.

`value`

Значення, що встановлюється. Число з точкою, що плаває, в діапазоні від 0 до 1.

### Значення, що повертаються

Об'єкт [GmagickPixel](class.gmagickpixel.html) у разі успішного виконання.