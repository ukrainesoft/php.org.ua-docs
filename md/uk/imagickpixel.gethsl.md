---
navigation:
  - imagickpixel.getcolorvaluequantum.md: '« ImagickPixel::getColorValueQuantum'
  - imagickpixel.getindex.md: 'ImagickPixel::getIndex »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::getHSL'
---
# ImagickPixel::getHSL

(PECL imagick 2, PECL imagick 3)

ImagickPixel::getHSL — Повертає нормалізований HSL колір об'єкту ImagickPixel

### Опис

```methodsynopsis
public ImagickPixel::getHSL(): array
```

Повертає нормалізований HSL-колір, описаний об'єктом ImagickPixel, кожне із трьох значень є дробовим числом між 0.0 та 1.0.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає HSL-значення у вигляді масиву з ключами "hue", "saturation" та "luminosity". У разі виникнення помилки буде викинуто виняток ImagickPixelException.

### Приклади

**Приклад #1 Приклад використання **Imagick::getHSL()****

```php
<?php

$color = new ImagickPixel('rgb(90%, 10%, 10%)');

$colorInfo = $color->getHSL();

print_r($colorInfo);

?>
```

Результат виконання цього прикладу:

```
Array
(
    [hue] => 0
    [saturation] => 0.80001220740379
    [luminosity] => 0.50000762951095
)
```

### Примітки

> **Зауваження**
> 
> Доступно з бібліотекою ImageMagick версії 6.2.9 або вищою.
