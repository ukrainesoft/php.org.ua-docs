Малює коло

-   [« ImagickDraw::bezier](imagickdraw.bezier.html)
    
-   [ImagickDraw::clear »](imagickdraw.clear.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює коло
    

# ImagickDraw::circle

(PECL imagick 2, PECL imagick 3)

ImagickDraw::circle — Малює коло

### Опис

```methodsynopsis
public ImagickDraw::circle(    float $ox,    float $oy,    float $px,    float $py): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює коло на зображенні.

### Список параметрів

`ox`

Вихідна координата X

`oy`

Вихідна координата Y

`px`

Координата X периметра

`py`

Координата Y периметра

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::circle()****

```php
<?php
function circle($strokeColor, $fillColor, $backgroundColor, $originX, $originY, $endX, $endY) {

    //Создание объекта ImagickDraw для рисования.
    $draw = new \ImagickDraw();

    $strokeColor = new \ImagickPixel($strokeColor);
    $fillColor = new \ImagickPixel($fillColor);

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    $draw->circle($originX, $originY, $endX, $endY);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```