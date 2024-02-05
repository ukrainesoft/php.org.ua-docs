---
navigation:
  - function.imagecolorset.md: « imagecolorset
  - function.imagecolorstotal.md: imagecolorstotal »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorsforindex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagecolorsforindex

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorsforindex — Отримання кольорів, що відповідають індексу

### Опис

```methodsynopsis
imagecolorsforindex(GdImage $image, int $color): array
```

Отримання кольорів, які відповідають заданому індексу.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`color`

Індекс кольору.

### Значення, що повертаються

Повертає асоціативний масив із червоним, зеленим, синім та альфа ключами, що містить відповідні значення для заданого індексу кольору.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |
| 8.0.0 | Функция**imagecolorsforindex()** тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `color` поза допустимим діапазоном; раніше натомість поверталося значення **`false`** |

### Приклади

**Пример #1 Пример использования**imagecolorsforindex()\*\*\*\*

```php
<?php

// открываем изображение
$im = imagecreatefrompng('nexen.png');

// получаем цвет
$start_x = 40;
$start_y = 50;
$color_index = imagecolorat($im, $start_x, $start_y);

// делаем его удобочитаемым
$color_tran = imagecolorsforindex($im, $color_index);

// что здесь ?
print_r($color_tran);

?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
   [red] => 226
   [green] => 222
   [blue] => 252
   [alpha] => 0
)
```

### Дивіться також

-   [imagecolorat()](function.imagecolorat.md) \- Отримання індексу кольору пікселя
-   [imagecolorexact()](function.imagecolorexact.md) \- Отримання індексу заданого кольору
