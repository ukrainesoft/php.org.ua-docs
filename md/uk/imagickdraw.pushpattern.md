---
navigation:
  - imagickdraw.pushdefs.md: '« ImagickDraw::pushDefs'
  - imagickdraw.rectangle.md: 'ImagickDraw::rectangle »'
  - index.md: PHP Manual
  - class.imagickdraw.md: ImagickDraw
title: 'ImagickDraw::pushPattern'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickDraw::pushPattern

(PECL imagick 2, PECL imagick 3)

ImagickDraw::pushPattern — Вказує, що наступні команди аж до ImagickDraw::opPattern() складають визначення іменованого патерну

### Опис

```methodsynopsis
public ImagickDraw::pushPattern(    string $pattern_id,    float $x,    float $y,    float $width,    float $height): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

Вказує, що наступні команди до DrawPopPattern() містять визначення іменованого патерну. Простору патерна призначаються координати верхнього лівого кута, ширина і висота, і він стає простором для малювання. Все, що можна намалювати, можна використовувати у визначенні патерну. Іменовані патерни можуть використовуватися як визначення обведення або кистей.

### Список параметрів

`pattern_id`

ID патерну.

`x`

Координата x лівого верхнього кута.

`y`

Координата у лівого верхнього кута.

`width`

Ширина патерну.

`height`

Висота патерну.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** ImagickDraw::pushPattern()\*\*\*\*

```php
<?php
function pushPattern($strokeColor, $fillColor, $backgroundColor) {
    $draw = new \ImagickDraw();

    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);
    $draw->setStrokeWidth(1);
    $draw->setStrokeOpacity(1);
    $draw->setStrokeColor($strokeColor);
    $draw->setFillColor($fillColor);

    $draw->setStrokeWidth(1);

    $draw->pushPattern("MyFirstPattern", 0, 0, 50, 50);
    for ($x = 0; $x < 50; $x += 10) {
        for ($y = 0; $y < 50; $y += 5) {
            $positionX = $x + (($y / 5) % 5);
            $draw->rectangle($positionX, $y, $positionX + 5, $y + 5);
        }
    }
    $draw->popPattern();

    $draw->setFillOpacity(0);
    $draw->rectangle(100, 100, 400, 400);
    $draw->setFillOpacity(1);

    $draw->setFillOpacity(1);

    $draw->push();
    $draw->setFillPatternURL('#MyFirstPattern');
    $draw->setFillColor('yellow');
    $draw->rectangle(100, 100, 400, 400);
    $draw->pop();

    $imagick = new \Imagick();
    $imagick->newImage(500, 500, $backgroundColor);
    $imagick->setImageFormat("png");

    $imagick->drawImage($draw);

    header("Content-Type: image/png");
    echo $imagick->getImageBlob();
}

?>
```
