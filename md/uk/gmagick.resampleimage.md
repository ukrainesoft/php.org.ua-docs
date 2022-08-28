Змінює роздільну здатність зображення до бажаного

-   [« Gmagick::removeimageprofile](gmagick.removeimageprofile.html)
    
-   [Gmagick::resizeimage »](gmagick.resizeimage.html)
    
-   [PHP Manual](index.html)
    
-   [Gmagick](class.gmagick.html)
    
-   Змінює роздільну здатність зображення до бажаного
    

# Gmagick::resampleimage

(PECL gmagick >= Unknown)

Gmagick::resampleimage — Змінює роздільну здатність зображення до бажаного.

### Опис

```methodsynopsis
public Gmagick::resampleimage(    float $xResolution,    float $yResolution,    int $filter,    float $blur): Gmagick
```

Змінює роздільну здатність зображення до бажаного.

### Список параметрів

`xResolution`

Нова роздільна здатність по осі x.

`yResolution`

Нова роздільна здатність по осі y.

`filter`

Фільтр зображень для використання.

`blur`

Коефіцієнт розмиття, де більше значення більше 1 робить зображення більш розмитим, значення менше 1 менш розмитим.

### Значення, що повертаються

Об'єкт [Gmagick](class.gmagick.html) у разі успішного виконання.

### Помилки

Викликає **GmagickException** у разі виникнення помилки.