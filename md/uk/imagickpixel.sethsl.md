---
navigation:
  - imagickpixel.setcolorvaluequantum.md: '« ImagickPixel::setColorValueQuantum'
  - imagickpixel.setindex.md: 'ImagickPixel::setIndex »'
  - index.md: PHP Manual
  - class.imagickpixel.md: ImagickPixel
title: 'ImagickPixel::setHSL'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ImagickPixel::setHSL

(PECL imagick 2, PECL imagick 3)

ImagickPixel::setHSL — Встановлення нормалізованого кольору HSL

### Опис

```methodsynopsis
public ImagickPixel::setHSL(float $hue, float $saturation, float $luminosity): bool
```

Встановлює колір в об'єкті ImagickPixel, використовуючи нормалізовані значення відтінку, насиченості та яскравості.

### Список параметрів

`hue`

Нормалізоване значення відтінку, як значення кругової веселки (між 0 і 1), де нульовим значенням буде червоний колір.

`saturation`

Нормалізоване значення насиченості, де означає повне насичення.

`luminosity`

Нормалізоване значення яскравості за шкалою від 0 (чорний) до 1 (білий), при встановленому HS у значенні 0.5.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Приклади

**Приклад #1 Приклад використання** ImagickPixel::setHSL()\*\*\*\*

```php
<?php

//Создание почти чистого красного цвета
$color = new ImagickPixel('rgb(90%, 10%, 10%)');

//Получение значений HSL
$colorInfo = $color->getHSL();

//Поворачиваем оттенок на 180 градусов
$newHue = $colorInfo['hue'] + 0.5;
if ($newHue > 1) {
    $newHue = $newHue - 1;
}

//Устанавливаем ImagickPixel в новый цвет
$colorInfo = $color->setHSL($newHue, $colorInfo['saturation'], $colorInfo['luminosity']);

//Проверяем, что новый цвет является голубым/зелёным
$colorInfo = $color->getcolor();
print_r($colorInfo);

?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [r] => 26
    [g] => 230
    [b] => 230
    [a] => 255
)
```

### Примітки

> **Зауваження** :
> 
> Доступно з версії 6.2.9 та вище бібліотеки ImageMagick.
