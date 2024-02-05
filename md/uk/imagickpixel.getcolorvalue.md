---
navigation:
  - imagickpixel.getcolorquantum.md: '« ImagickPixel::getColorQuantum'
  - imagickpixel.getcolorvaluequantum.md: 'ImagickPixel::getColorValueQuantum »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getColorValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::getColorValue

(PECL imagick 2, PECL imagick 3)

ImagickPixel::getColorValue — Повертає нормалізоване значення кольору каналу

### Опис

```methodsynopsis
public ImagickPixel::getColorValue(int $color): float
```

Повертає значення зазначеного кольору каналу як дробове число між 0 і 1.

### Список параметрів

`color`

Колір, для якого виходить значення, задане однією з констант Imagick. Це RGB колір, CMYK колір, альфа канал або прозорість (Imagick::COLOR\_BLUE, Imagick::COLOR\_MAGENTA);

### Значення, що повертаються

Значення каналу, як нормалізованого дробового числа, у разі виникнення помилки буде викинуто виняток ImagickPixelException.

### Приклади

**Приклад #1 Приклад використання** Imagick::getColorValue()\*\*\*\*

```php
<?php

$color = new ImagickPixel('rgba(90%, 20%, 20%, 0.75)');

echo "Значение альфа канала ".$color->getColorValue(Imagick::COLOR_ALPHA).PHP_EOL;
echo "".PHP_EOL;
echo "Значение красного канала ".$color->getColorValue(Imagick::COLOR_RED).PHP_EOL;
echo "Значение зелёного канала ".$color->getColorValue(Imagick::COLOR_GREEN).PHP_EOL;
echo "Значение синего канала ".$color->getColorValue(Imagick::COLOR_BLUE).PHP_EOL;
echo "".PHP_EOL;
echo "Значение голубого канала ".$color->getColorValue(Imagick::COLOR_CYAN).PHP_EOL;
echo "Значение пурпурного канала ".$color->getColorValue(Imagick::COLOR_MAGENTA).PHP_EOL;
echo "Значение жёлтого канала ".$color->getColorValue(Imagick::COLOR_YELLOW).PHP_EOL;
echo "Значение чёрного канала ".$color->getColorValue(Imagick::COLOR_BLACK).PHP_EOL;

?>
```

Результат виконання наведеного прикладу:

```
Значение альфа канала 0.74999618524453

Значение красного канала 0.90000762951095
Значение зелёного канала 0.2
Значение синего канала 0.2

Значение голубого канала 0.90000762951095
Значение пурпурного канала 0.2
Значение жёлтого канала 0.2
Значение чёрного канала 0
```
