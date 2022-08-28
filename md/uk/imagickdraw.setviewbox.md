Встановлює загальний розмір полотна

-   [« ImagickDraw::setVectorGraphics](imagickdraw.setvectorgraphics.html)
    
-   [ImagickDraw::skewX »](imagickdraw.skewx.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Встановлює загальний розмір полотна
    

# ImagickDraw::setViewbox

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setViewbox — Встановлює загальний розмір полотна

### Опис

```methodsynopsis
public ImagickDraw::setViewbox(    int $x1,    int $y1,    int $x2,    int $y2): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює загальний розмір полотна, яке буде записано з векторними даними малюнка. Зазвичай використовується розмір зображення полотна. Коли векторні дані зберігаються у форматах SVG або MVG, вікно перегляду використовується для визначення розміру зображення полотна, на якому засіб перегляду відображатиме векторні дані.

### Список параметрів

`x1`

Ліва координата x.

`y1`

Ліва координата y.

`x2`

Права координата x.

`y2`

Права координата y.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setViewBox()****

```php
<?php
function setViewBox($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);

    /*

    Устанавливает общий размер холста, который будет записан с векторными данными рисунка. Обычно для этого используется размер изображения холста. Когда векторные данные сохраняются в форматах SVG или MVG, окно просмотра используется для указания размера изображения холста, на котором средство просмотра будет отображать векторные данные.

     */

    $draw->circle(250, 250, 250, 0);
    $draw->setviewbox(0, 0, 200, 200);
    $draw->circle(125, 250, 250, 250);
    $draw->translate(250, 125);
    $draw->circle(0, 0, 125, 0);


    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```