Керує згладжуванням тексту

-   [« ImagickDraw::setTextAlignment](imagickdraw.settextalignment.html)
    
-   [ImagickDraw::setTextDecoration »](imagickdraw.settextdecoration.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Керує згладжуванням тексту
    

# ImagickDraw::setTextAntialias

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setTextAntialias — Керує згладжуванням тексту

### Опис

```methodsynopsis
public ImagickDraw::setTextAntialias(bool $antiAlias): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Керує згладжуванням тексту. За промовчанням текст згладжується.

### Список параметрів

`antiAlias`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setTextAntialias()****

```php
<?php
function setTextAntialias($fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor('none');
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setFontSize(32);
    $draw->setTextAntialias(false);
    $draw->annotation(5, 30, "Lorem Ipsum!");
    $draw->setTextAntialias(true);
    $draw->annotation(5, 65, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(220, 80, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    //Scale the image so that people can see the aliasing.
    $imagick->scaleImage(220 * 6, 80 * 6);
    $imagick->cropImage(640, 480, 0, 0);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```