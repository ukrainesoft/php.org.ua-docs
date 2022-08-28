Малює ламану лінію

-   [« ImagickDraw::polygon](imagickdraw.polygon.html)
    
-   [ImagickDraw::pop »](imagickdraw.pop.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює ламану лінію
    

# ImagickDraw::polyline

(PECL imagick 2, PECL imagick 3)

ImagickDraw::polyline — Малює ламану лінію

### Опис

```methodsynopsis
public ImagickDraw::polyline(array $coordinates): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює ламану лінію з використанням поточної обведення, її ширини, кольору заливки або текстури з використанням масиву координат.

### Список параметрів

`coordinates`

Масив координат x та y: array( array( 'x' => 4, 'y' => 6 ), array( 'x' => 8, 'y' => 10 ) )

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::polyline()****

```php
<?php
function polyline($strokeColor, $fillColor, $backgroundColor) {
    $draw = new \ImagickDraw();

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(5);

    $points = [
        ['x' => 40 * 5, 'y' => 10 * 5],
        ['x' => 20 * 5, 'y' => 20 * 5],
        ['x' => 70 * 5, 'y' => 50 * 5],
        ['x' => 60 * 5, 'y' => 15 * 5]
    ];

    $draw->polyline($points);

    $image = new \Imagick();
    $image->newImage(500, 300, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```