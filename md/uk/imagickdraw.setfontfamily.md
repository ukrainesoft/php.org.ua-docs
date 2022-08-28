Встановлює сімейство шрифтів для використання при анотуванні текстом

-   [« ImagickDraw::setFont](imagickdraw.setfont.html)
    
-   [ImagickDraw::setFontSize »](imagickdraw.setfontsize.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Встановлює сімейство шрифтів для використання при анотуванні текстом
    

# ImagickDraw::setFontFamily

(PECL imagick 2, PECL imagick 3)

ImagickDraw::setFontFamily — Встановлює сімейство шрифтів для використання при анотуванні текстом

### Опис

```methodsynopsis
public ImagickDraw::setFontFamily(string $font_family): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Встановлює сімейство шрифтів для використання під час анотування текстом.

### Список параметрів

`font_family`

Сімейство шрифтів.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::setFontFamily()****

```php
<?php
function setFontFamily($fillColor, $strokeColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $strokeColor = new \ImagickPixel($strokeColor);
    $fillColor = new \ImagickPixel($fillColor);

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(2);

    $draw->setFontSize(48);

    $draw->setFontFamily("Times");
    $draw->annotation(50, 50, "Lorem Ipsum!");

    $draw->setFontFamily("AvantGarde");
    $draw->annotation(50, 100, "Lorem Ipsum!");

    $draw->setFontFamily("NewCenturySchlbk");
    $draw->annotation(50, 150, "Lorem Ipsum!");

    $draw->setFontFamily("Palatino");
    $draw->annotation(50, 200, "Lorem Ipsum!");

    $imagick = new \Imagick();
    $imagick->newImage(450, 250, $backgroundColor);
    $imagick->setImageFormat("png");
    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```