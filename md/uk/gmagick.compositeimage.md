Накладає одне зображення на інше

-   [« Gmagick::commentimage](gmagick.commentimage.html)
    
-   [Gmagick::construct »](gmagick.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Накладає одне зображення на інше
    

# Gmagick::compositeimage

(PECL gmagick >= Unknown)

Gmagick::compositeimage — Накладає одне зображення на інше

### Опис

```methodsynopsis
public Gmagick::compositeimage(    Gmagick $source,    int $COMPOSE,    int $x,    int $y): Gmagick
```

Накладає одне зображення на інше із зазначеним усуненням.

### Список параметрів

`source`

Об'єкт [Gmagick](class.gmagick.html), що містить складне зображення.

`compose`

Композитний оператор.

`x`

Усунення стовпця складеного зображення.

`y`

Зміщення рядка складеного зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) із композиціями.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.