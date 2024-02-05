---
navigation:
  - function.imagepolygon.md: « imagepolygon
  - function.imageresolution.md: imageresolution »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagerectangle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagerectangle

(PHP 4, PHP 5, PHP 7, PHP 8)

imagerectangle - Малювання прямокутника

### Опис

```methodsynopsis
imagerectangle(    GdImage $image,    int $x1,    int $y1,    int $x2,    int $y2,    int $color): bool
```

**imagerectangle()** малює прямокутник із заданими координатами кутів.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x1`

Верхня ліва x координата.

`y1`

Верхня ліва y координата 0, 0 – лівий верхній кут зображення.

`x2`

Нижня права x координата.

`y2`

Нижня права y координата.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Пример #1 Пример использования**imagerectangle()\*\*\*\*

```php
<?php
// Создание изображения 200 x 200
$canvas = imagecreatetruecolor(200, 200);

// Создание цветов
$pink = imagecolorallocate($canvas, 255, 105, 180);
$white = imagecolorallocate($canvas, 255, 255, 255);
$green = imagecolorallocate($canvas, 132, 135, 28);

// Рисование разноцветных прямоугольников
imagerectangle($canvas, 50, 50, 150, 150, $pink);
imagerectangle($canvas, 45, 60, 120, 100, $white);
imagerectangle($canvas, 100, 120, 75, 160, $green);

// Вывод и освобождение памяти
header('Content-Type: image/jpeg');

imagejpeg($canvas);
imagedestroy($canvas);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagerectangle()](images/21009b70229598c6a80eef8b45bf282b-imagerectangle.jpg)
