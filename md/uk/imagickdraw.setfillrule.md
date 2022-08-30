Встановлює правило заливання для використання під час малювання полігонів.

-   [« ImagickDraw::setFillPatternURL](imagickdraw.setfillpatternurl.md)
    
-   [ImagickDraw::setFont »](imagickdraw.setfont.md)
    
-   [PHP Manual](index.md)
    
-   [ImagickDraw](class.imagickdraw.md)
    
-   Встановлює правило заливання для використання під час малювання полігонів.
    

# ImagickDraw::setFillRule

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFillRule - Встановлює правило заливання для використання при малюванні полігонів

### Опис

```methodsynopsis
public ImagickDraw::setFillRule(int $fill_rule): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює правило заливання для використання під час малювання полігонів.

### Список параметрів

`fill_rule`

Одна з констант [FILLRULE](imagick.constants.html#imagick.constants.fillrule) `imagick::FILLRULE_*`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setFillRule()****

```php
<?php
function setFillRule($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeWidth(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $fillRules = [\Imagick::FILLRULE_NONZERO, \Imagick::FILLRULE_EVENODD];

    $points = 11;
    $size = 150;

    $draw->translate(175, 160);

    for ($x = 0; $x < 2; $x++) {
        $draw->setFillRule($fillRules[$x]);
        $draw->pathStart();
        for ($n = 0; $n < $points * 2; $n++) {

            if ($n >= $points) {
                $angle = fmod($n * 360 * 4 / $points, 360) * pi() / 180;
            }
            else {
                $angle = fmod($n * 360 * 3 / $points, 360) * pi() / 180;
            }

            $positionX = $size * sin($angle);
            $positionY = $size * cos($angle);

            if ($n == 0) {
                $draw->pathMoveToAbsolute($positionX, $positionY);
            }
            else {
                $draw->pathLineToAbsolute($positionX, $positionY);
            }
        }

        $draw->pathClose();
        $draw->pathFinish();

        $draw->translate(325, 0);
    }

    $image = new \Imagick();
    $image->newImage(700, 320, $backgroundColor);
    $image->setImageFormat("png");
    $image->drawImage($draw);

    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```