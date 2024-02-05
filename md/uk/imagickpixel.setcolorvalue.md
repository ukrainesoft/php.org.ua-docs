---
navigation:
  - imagickpixel.setcolorcount.md: '« ImagickPixel::setColorCount'
  - imagickpixel.setcolorvaluequantum.md: 'ImagickPixel::setColorValueQuantum »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::setColorValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::setColorValue

(PECL imagick 2, PECL imagick 3)

ImagickPixel::setColorValue — Встановлює нормалізоване значення одного з каналів

### Опис

```methodsynopsis
public ImagickPixel::setColorValue(int $color, float $value): bool
```

Встановлює значення вказаного каналу поточного об'єкта за умови, що нове значення знаходиться між 0 і 1. Ця функція може бути використана для встановлення прозорості каналу об'єкта ImagickPixel.

### Список параметрів

`color`

Одна из констант цвета Imagick, т.е\\Imagick::COLOR\_GREEN или\\Imagick::COLOR\_ALPHA.

`value`

Значення для встановлення у цьому каналі, в межах від 0 до 1.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Пример #1 Пример использования**Imagick::setColorValue()\*\*\*\*

```php
<?php

$color  = new \ImagickPixel('firebrick');

$color->setColorValue(Imagick::COLOR_ALPHA, 0.5);

print_r($color->getcolor(true));
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [r] => 0.69803921568627
    [g] => 0.13333333333333
    [b] => 0.13333333333333
    [a] => 0.50000762951095
)
```
