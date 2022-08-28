Застосовує зазначений поворот до поточного координатного простору

-   [« ImagickDraw::resetVectorGraphics](imagickdraw.resetvectorgraphics.html)
    
-   [ImagickDraw::roundRectangle »](imagickdraw.roundrectangle.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Застосовує зазначений поворот до поточного координатного простору
    

# ImagickDraw::rotate

(PECL imagick 2, PECL imagick 3)

ImagickDraw::rotate — Застосовує вказаний поворот до поточного координатного простору.

### Опис

```methodsynopsis
public ImagickDraw::rotate(float $degrees): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Застосовує зазначений поворот до координатного простору.

### Список параметрів

`degrees`

Кут повороту.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::rotate()****

```php
<?php
function rotate($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor) {
    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeOpacity(1);
    $draw->setFillColor($fillColor);
    $draw->rectangle(200, 200, 300, 300);
    $draw->setFillColor($fillModifiedColor);
    $draw->rotate(15);
    $draw->rectangle(200, 200, 300, 300);

    $image = new \Imagick();
    $image->newImage(500, 500, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```