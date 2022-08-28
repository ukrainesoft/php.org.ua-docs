Застосовує перенесення до поточної системи координат

-   [« ImagickDraw::skewY](imagickdraw.skewy.html)
    
-   [ImagickPixel »](class.imagickpixel.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Застосовує перенесення до поточної системи координат
    

# ImagickDraw::translate

(PECL imagick 2, PECL imagick 3)

ImagickDraw::translate — Застосовує перенесення до поточної системи координат

### Опис

```methodsynopsis
public ImagickDraw::translate(float $x, float $y): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Застосовує перенесення до поточної системи координат, яка переміщає початок системи координат у зазначену координату.

### Список параметрів

`x`

Горизонтальне перенесення.

`y`

Вертикальне перенесення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::translate()****

```php
<?php
function translate($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor,
                   $startX, $startY, $endX, $endY, $translateX, $translateY) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->rectangle($startX, $startY, $endX, $endY);

    $draw->setFillColor($fillModifiedColor);
    $draw->translate($translateX, $translateY);
    $draw->rectangle($startX, $startY, $endX, $endY);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");

    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```