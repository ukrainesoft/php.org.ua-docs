---
navigation:
  - imagickdraw.poppattern.md: '« ImagickDraw::popPattern'
  - imagickdraw.pushclippath.md: 'ImagickDraw::pushClipPath »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::push'
---
# ImagickDraw::push

(PECL imagick 2, PECL imagick 3)

ImagickDraw::push — Клонує поточний об'єкт ImagickDraw і додає його до стек

### Опис

```methodsynopsis
public ImagickDraw::push(): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

Клонує поточний об'єкт ImagickDraw для створення нового об'єкта ImagickDraw, який потім додається до стек ImagickDraw. Вихідний об'єкт ImagickDraw (або кілька об'єктів) можна повернути, викликавши [ImagickDraw::pop()](imagickdraw.pop.md). Об'єкти ImagickDraw зберігаються у стеку ImagickDraw. Для кожної операції видалення має бути еквівалентна операція додавання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ImagickDraw::push()****

```php
<?php
function push($strokeColor, $fillColor, $backgroundColor, $fillModifiedColor) {

    $draw = new \ImagickDraw();
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillModifiedColor);
    $draw->setStrokeWidth(2);
    $draw->setFontSize(72);
    $draw->push();
    $draw->translate(50, 50);
    $draw->rectangle(200, 200, 300, 300);
    $draw->pop();
    $draw->setFillColor($fillColor);
    $draw->rectangle(200, 200, 300, 300);

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
