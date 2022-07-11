- [« ImagickDraw::arc](imagickdraw.arc.md)
- [ImagickDraw::circle »](imagickdraw.circle.md)

- [PHP Manual](index.md)
- [ImagickDraw](class.imagickdraw.md)
- Малює криву Безьє

# ImagickDraw::bezier

(PECL imagick 2, PECL imagick 3)

ImagickDraw::bezier — Малює криву Без'є

### Опис

public **ImagickDraw::bezier**(array `$coordinates`): bool

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

Малює криву Безьє через набір точок на зображенні.

### Список параметрів

`coordinates`
Багатомірний масив на кшталт array( array( 'x' =\> 1, 'y' =\> 2 ), array(
'x' =\> 3, 'y' =\> 4))

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::bezier()****

` <?phpfunction bezier($strokeColor, $fillColor, $backgroundColor) {    $draw = new \ImagickDraw(); $strokeColor= new \ImagickPixel($strokeColor); $fillColor= new \ImagickPixel($fillColor); $draw->setStrokeOpacity(1); $draw->setStrokeColor($strokeColor); $draw->setFillColor($fillColor); $draw->setStrokeWidth(2); $smoothPointsSet = [        [            ['x' => 10.0 * 5, 'y' => 10.0 * 5],            ['x' => 30.0 * 5, 'y' => 90.0 * 5],            ['x' = > 25.0 * 5, 'y' => 10.0 * 5],            ['x' => 50.0 * 5, 'y' => 50.0 * 5],        ],        [            ['x' => 50.0 * 5, 'y ' => 50.0 * 5],            ['x' => 75.0 * 5, 'y' => 90.0 * 5],            ['x' => 70.0 * 5, 'y' => 10.0 * 5],            [' x' => 90.0 * 5, 'y' => 40.0 * 5],        ],    ]; foreach ($smoothPointsSet as $points) {        $draw->bezier($points); }    $disjointPoints = [        [            ['x' => 10 * 5, 'y' => 10 * 5],            ['x' => 30 * 5, 'y' => 90 * 5],            ['x' => 25 * 5, 'y' => 10 * 5],            ['x' => 50 * 5, 'y' => 50 * 5],        ],        [            ['x' => 50 * 5, ' y' => 50 * 5],            ['x' => 80 * 5, 'y' => 50 * 5],            ['x' => 70 * 5, 'y' => 10 * 5],            [ 'x' => 90 * 5, 'y' => 40 * 5],         ]    ]; $draw->translate(0, 200); foreach ($disjointPoints as $points) {        $draw->bezier($points); }    //Створення об'єкта зображення, в можна перетворити команди малювання. $imagick==newImagick(); $imagick->newImage(500, 500, $backgroundColor); $imagick->setImageFormat("png"); //Перетворення команд малювання в об'єкті ImagickDraw    //в зображення. $imagick->drawImage($draw); //Відображення зображення в браузері   header("Content-Type:image/png"); echo $imagick->getImageBlob();}?> `
