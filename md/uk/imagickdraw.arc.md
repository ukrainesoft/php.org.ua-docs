---
navigation:
  - imagickdraw.annotation.md: '« ImagickDraw::annotation'
  - imagickdraw.bezier.md: 'ImagickDraw::bezier »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::arc'
---
# ImagickDraw::arc

(PECL imagick 2, PECL imagick 3)

ImagickDraw::arc — Малює дугу

### Опис

```methodsynopsis
public ImagickDraw::arc(    float $sx,    float $sy,    float $ex,    float $ey,    float $sd,    float $ed): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Малює дугу, що потрапляє у вказаний прямокутник на зображенні.

### Список параметрів

`sx`

Початкова координата X прямокутника, що обмежує

`sy`

Початкова координата Y прямокутника, що обмежує

`ex`

Кінцева координата X прямокутника, що обмежує

`ey`

Кінцева координата Y обмежує прямокутника

`sd`

Початковий градус обертання

`ed`

Кінцевий градус обертання

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::arc()****

```php
<?php
function arc($strokeColor, $fillColor, $backgroundColor, $startX, $startY, $endX, $endY, $startAngle, $endAngle) {

    //Создание объекта ImagickDraw для рисования.
    $draw = new \ImagickDraw();
    $draw->setStrokeWidth(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(2);

    $draw->arc($startX, $startY, $endX, $endY, $startAngle, $endAngle);

    //Создание объекта изображения, в который можно преобразовать команды рисования.
    $image = new \Imagick();
    $image->newImage(IMAGE_WIDTH, IMAGE_HEIGHT, $backgroundColor);
    $image->setImageFormat("png");

    //Преобразование команд рисования в объекте ImagickDraw
    //в изображение.
    $image->drawImage($draw);

    //Отображение изображения в браузере
    header("Content-Type: image/png");
    echo $image->getImageBlob();
}

?>
```
