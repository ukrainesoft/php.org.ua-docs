Накладає зображення на поточне зображення

-   [« ImagickDraw::comment](imagickdraw.comment.html)
    
-   [ImagickDraw::\_\_construct »](imagickdraw.construct.html)
    
-   [PHP Manual](index.html)
    
-   [ImagickDraw](class.imagickdraw.html)
    
-   Накладає зображення на поточне зображення
    

# ImagickDraw::composite

(PECL imagick 2, PECL imagick 3)

ImagickDraw::composite — Накладає зображення на поточне зображення

### Опис

```methodsynopsis
public ImagickDraw::composite(    int $compose,    float $x,    float $y,    float $width,    float $height,    Imagick $compositeWand): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Накладає зображення на поточне зображення, використовуючи вказаний оператор накладання, вказану позицію та вказаний розмір.

### Список параметрів

`compose`

Оператор накладання. Одна з констант [Оператора накладывания](imagick.constants.html#imagick.constants.compositeop) `imagick::COMPOSITE_*`

`x`

Координата X лівого верхнього кута.

`y`

Координата Y лівого верхнього кута.

`width`

Ширина зображення композиції.

`height`

Висота зображення композиції.

`compositeWand`

Об'єкт [Imagick](class.imagick.html), З якого взято композиційне зображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::composite()****

```php
<?php
function composite($strokeColor, $fillColor, $backgroundColor) {

    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setFillOpacity(1);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setStrokeWidth(2);
    $draw->setFont("../fonts/CANDY.TTF");
    $draw->setFontSize(140);
    $draw->rectangle(0, 0, 1000, 300);
    $draw->setFillColor('white');
    $draw->setfillopacity(1);
    $draw->annotation(50, 180, "Lorem Ipsum!");

    //Создание объекта изображения, в который можно преобразовать команды рисования.
    $imagick = new \Imagick();
    $imagick->newImage(1000, 302, $backgroundColor);
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