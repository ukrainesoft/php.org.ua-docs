Малює криву Безьє

-   [« ImagickDraw::arc](imagickdraw.arc.html)
    
-   [ImagickDraw::circle »](imagickdraw.circle.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Малює криву Безьє
    

# ImagickDraw::bezier

(PECL imagick 2, PECL imagick 3)

ImagickDraw::bezier — Малює криву Безьє

### Опис

```methodsynopsis
public ImagickDraw::bezier(array $coordinates): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює криву Безьє через набір точок на зображенні.

### Список параметрів

`coordinates`

Багатовимірний масив на кшталт array( array( 'x' => 1, 'y' => 2 ), array( 'x' => 3, 'y' => 4 ) )

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::bezier()****

```php
<?php
function bezier($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $strokeColor = new \ImagickPixel($strokeColor);
    $fillColor = new \ImagickPixel($fillColor);

    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);

    $smoothPointsSet = [
        [
            ['x' => 10.0 * 5, 'y' => 10.0 * 5],
            ['x' => 30.0 * 5, 'y' => 90.0 * 5],
            ['x' => 25.0 * 5, 'y' => 10.0 * 5],
            ['x' => 50.0 * 5, 'y' => 50.0 * 5],
        ],
        [
            ['x' => 50.0 * 5, 'y' => 50.0 * 5],
            ['x' => 75.0 * 5, 'y' => 90.0 * 5],
            ['x' => 70.0 * 5, 'y' => 10.0 * 5],
            ['x' => 90.0 * 5, 'y' => 40.0 * 5],
        ],
    ];

    foreach ($smoothPointsSet as $points) {
        $draw->bezier($points);
    }

    $disjointPoints = [
        [
            ['x' => 10 * 5, 'y' => 10 * 5],
            ['x' => 30 * 5, 'y' => 90 * 5],
            ['x' => 25 * 5, 'y' => 10 * 5],
            ['x' => 50 * 5, 'y' => 50 * 5],
        ],
        [
            ['x' => 50 * 5, 'y' => 50 * 5],
            ['x' => 80 * 5, 'y' => 50 * 5],
            ['x' => 70 * 5, 'y' => 10 * 5],
            ['x' => 90 * 5, 'y' => 40 * 5],
         ]
    ];
    $draw->translate(0, 200);

    foreach ($disjointPoints as $points) {
        $draw->bezier($points);
    }

    //Создание объекта изображения, в который можно преобразовать команды рисования.
    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    //Преобразование команд рисования в объекте ImagickDraw
    //в изображение.
    $imagick->drawImage($draw);

    //Отображение изображения в браузере
    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```