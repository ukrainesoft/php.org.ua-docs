Повертає зображення

-   [« Gmagick::rollimage](gmagick.rollimage.html)
    
-   [Gmagick::scaleimage »](gmagick.scaleimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Повертає зображення
    

# Gmagick::rotateimage

(PECL gmagick >= Unknown)

Gmagick::rotateimage — Повертає зображення

### Опис

```methodsynopsis
public Gmagick::rotateimage(mixed $color, float $degrees): Gmagick
```

Повертає зображення на вказану кількість градусів. Порожні трикутники, що залишилися від повороту зображення, заповнюються кольором тла.

### Список параметрів

`color`

Піксель фону.

`degrees`

Число градусів для повороту зображення.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.