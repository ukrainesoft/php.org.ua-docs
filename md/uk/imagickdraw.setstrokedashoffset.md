Задає зміщення у штриховому патерні для початку штрихування

-   [« ImagickDraw::setStrokeDashArray](imagickdraw.setstrokedasharray.html)
    
-   [ImagickDraw::setStrokeLineCap »](imagickdraw.setstrokelinecap.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Задає зміщення у штриховому патерні для початку штрихування
    

# ImagickDraw::setStrokeDashOffset

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setStrokeDashOffset — Задає зміщення в штриховому патерні для початку штрихування

### Опис

```methodsynopsis
public ImagickDraw::setStrokeDashOffset(float $dash_offset): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Задає усунення в штриховому патерні для початку штрихування.

### Список параметрів

`dash_offset`

Зміщення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setStrokeDashOffset()****

```php
<?php
function setStrokeDashOffset($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(4);
    $draw->setStrokeDashArray([20, 20]);
    $draw->setStrokeDashOffset(0);
    $draw->rectangle(100, 50, 225, 175);

    //Начало эффекта штриховки в середине сплошной части
    $draw->setStrokeDashOffset(10);
    $draw->rectangle(275, 50, 400, 175);

    //Начало эффекта штриховки в пространственной части
    $draw->setStrokeDashOffset(20);
    $draw->rectangle(100, 200, 225, 350);
    $draw->setStrokeDashOffset(5);
    $draw->rectangle(275, 200, 400, 350);

    $image = new \Imagick();
    $image->newImage(500, 400, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```