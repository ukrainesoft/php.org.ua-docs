---
navigation:
  - function.imagefilledellipse.md: « imagefilledellipse
  - function.imagefilledrectangle.md: imagefilledrectangle »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagefilledpolygon
---
# imagefilledpolygon

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefilledpolygon — Малювання зафарбованого багатокутника

### Опис

Сигнатура починаючи з PHP 8.0.0 (не підтримується з іменованими аргументами)

```methodsynopsis
imagefilledpolygon(GdImage $image, array $points, int $color): bool
```

Альтернативний синтаксис (оголошений застарілим із PHP 8.1.0)

```methodsynopsis
imagefilledpolygon(    GdImage $image,    array $points,    int $num_points,    int $color): bool
```

**imagefilledpolygon()** створює зафарбований багатокутник у заданому зображенні `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`points`

Масив, що містить `x` і `y` координати послідовних вершин багатокутника

`num_points`

Загальна кількість точок (вершин) повинна бути не менше 3.

Якщо цей параметр опущено (дивіться альтернативний синтаксис), то масив `points` повинен містити парну кількість елементів і `num_points` буде обчислено як `count($points)/2`

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `num_points` оголошено застарілим. |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagefilledpolygon()****

```php
<?php
// задание Масива точек для многоугольника
$values = array(
            40,  50,  // Point 1 (x, y)
            20,  240, // Point 2 (x, y)
            60,  60,  // Point 3 (x, y)
            240, 20,  // Point 4 (x, y)
            50,  40,  // Point 5 (x, y)
            10,  10   // Point 6 (x, y)
            );

// создание изображения
$image = imagecreatetruecolor(250, 250);

// определение цветов
$bg   = imagecolorallocate($image, 0, 0, 0);
$blue = imagecolorallocate($image, 0, 0, 255);

// заливка фона
imagefilledrectangle($image, 0, 0, 249, 249, $bg);

// рисование многоугольника
imagefilledpolygon($image, $values, 6, $blue);

// вывод изображения
header('Content-type: image/png');
imagepng($image);
imagedestroy($image);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefilledpolygon()](images/21009b70229598c6a80eef8b45bf282b-imagefilledpolygon.png)

### Дивіться також

-   [imagepolygon()](function.imagepolygon.md) - Малювання багатокутника
