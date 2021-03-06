- [« ImagickDraw::setFontWeight](imagickdraw.setfontweight.md)
- [ImagickDraw::setResolution »](imagickdraw.setresolution.md)

- [PHP Manual](index.md)
- [ImagickDraw](class.imagickdraw.md)
- Встановлює гравітацію розміщення тексту

# ImagickDraw::setGravity

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setGravity — Встановлює гравітацію розміщення тексту

### Опис

public **ImagickDraw::setGravity**(int `$gravity`): bool

**Увага**

На цей час ця функція ще була документована; для
ознайомлення доступний лише список аргументів.

Встановлює гравітацію розміщення тексту, що використовується під час його
анотації.

### Список параметрів

`gravity`
Одна з констант
[GRAVITY](imagick.constants.md#imagick.constants.gravity)
(`imagick::GRAVITY_*`).

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setGravity()****

` <?phpfunction setGravity($fillColor, $strokeColor, $backgroundColor) {   $draw = new \ImagickDraw(); $draw->setStrokeColor($strokeColor); $draw->setFillColor($fillColor); $draw->setStrokeWidth(1); $draw->setFontSize(24); $gravitySettings = array(        \Imagick::GRAVITY_NORTHWEST => 'NorthWest',        \Imagick::GRAVITY_NORTH => 'North',        \Imagick::GRAVITY_NORTHEAST => 'NorthEast',        \Imagick::GRAVITY_WEST => 'West',        \ Imagick::GRAVITY_CENTER => 'Centre',        \Imagick::GRAVITY_SOUTHWEST => 'SouthWest',        \Imagick::GRAVITY_SOUTH => 'South',        \Imagick::GRAVITY_SOUTHEAST => 'SouthEast',        \Imagick::GRAVITY_EAST => 'East'    ); $draw->setFont("../fonts/Arial.ttf"); foreach ($gravitySettings as $type => $description) {        $draw->setGravity($type); $draw->annotation(50, 50, '"' . $description . '"'); }   $imagick = new \Imagick(); $imagick->newImage(500, 500, $backgroundColor); $imagick->setImageFormat("png"); $imagick->drawImage($draw); header("Content-Type: image/png"); echo $imagick->getImageBlob();}?> `
