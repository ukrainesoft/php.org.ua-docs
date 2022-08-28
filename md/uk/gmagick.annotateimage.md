Підписати зображення текстом

-   [« Gmagick::addnoiseimage](gmagick.addnoiseimage.html)
    
-   [Gmagick::blurimage »](gmagick.blurimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Підписати зображення текстом
    

# Gmagick::annotateimage

(PECL gmagick >= Unknown)

Gmagick::annotateimage — Підписати зображення текстом

### Опис

```methodsynopsis
public Gmagick::annotateimage(    GmagickDraw $GmagickDraw,    float $x,    float $y,    float $angle,    string $text): Gmagick
```

Підписати зображення тексту.

### Список параметрів

`GmagickDraw`

Об'єкт [GmagickDraw](class.gmagickdraw.html), що містить параметри для відображення тексту.

`x`

Горизонтальне зміщення лівого краю тексту в пікселях.

`y`

Вертикальне зміщення базової лінії тексту на пікселях.

`angle`

Кут під яким розміщувати текст.

`text`

Текст.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) з доданою інструкцією.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.