---
navigation:
  - function.imageellipse.md: « imageellipse
  - function.imagefilledarc.md: imagefilledarc »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefill
---
# imagefill

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefill - Заливка

### Опис

```methodsynopsis
imagefill(    GdImage $image,    int $x,    int $y,    int $color): bool
```

Виготовляє заливку, починаючи із заданих координат (верхній лівий кут має координати 0, 0), кольором `color` у зображенні `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x`

x-координата початку.

`y`

y-координата початку.

`color`

Колір заливки. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagefill()****

```php
<?php

$im = imagecreatetruecolor(100, 100);

// установка красного фона
$red = imagecolorallocate($im, 255, 0, 0);
imagefill($im, 0, 0, $red);

header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefill()](images/21009b70229598c6a80eef8b45bf282b-imagefill.png)

### Дивіться також

-   [imagecolorallocate()](function.imagecolorallocate.md) - Створення кольору для зображення
