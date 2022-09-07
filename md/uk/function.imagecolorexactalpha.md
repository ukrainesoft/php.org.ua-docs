---
navigation:
  - function.imagecolorexact.md: « imagecolorexact
  - function.imagecolormatch.md: imagecolormatch »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagecolorexactalpha
---
# imagecolorexactalpha

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagecolorexactalpha — Отримання індексу заданого кольору та альфа компонента

### Опис

```methodsynopsis
imagecolorexactalpha(    GdImage $image,    int $red,    int $green,    int $blue,    int $alpha): int
```

Повертає індекс для заданого кольору та альфа компонента на панелі зображення.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

`alpha`

Значення в діапазоні від `0` до `127`. . `0` означає непрозорість, `127` означає абсолютну прозорість.

Параметри кольору можуть бути цілими в діапазоні від 0 до 255, або шістнадцятковими в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Повертає індекс для заданого кольору та альфа компонента на панелі зображення або -1, якщо такого кольору на палітрі немає.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Отримання кольорів GD логотипу**

```php
<?php

// создание изображения
$im = imagecreatefrompng('./gdlogo.png');

$colors   = Array();
$colors[] = imagecolorexactalpha($im, 255, 0, 0, 0);
$colors[] = imagecolorexactalpha($im, 0, 0, 0, 127);
$colors[] = imagecolorexactalpha($im, 255, 255, 255, 55);
$colors[] = imagecolorexactalpha($im, 100, 255, 52, 20);

print_r($colors);

// освобождение памяти
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => 16711680
    [1] => 2130706432
    [2] => 939524095
    [3] => 342163252
)
```

### Дивіться також

-   [imagecolorclosestalpha()](function.imagecolorclosestalpha.md) - Отримання індексу кольору найближчого до заданого з урахуванням прозорості
