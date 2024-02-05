---
navigation:
  - function.imagepng.md: « imagepng
  - function.imagerectangle.md: imagerectangle »
  - index.md: PHP Manual
  - ref.image.md: Функції GD та функції для роботи із зображеннями
title: imagepolygon
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# imagepolygon

(PHP 4, PHP 5, PHP 7, PHP 8)

imagepolygon - Малювання багатокутника

### Опис

Сигнатура починаючи з PHP 8.0.0 (не підтримується з іменованими аргументами)

```methodsynopsis
imagepolygon(GdImage $image, array $points, int $color): bool
```

Альтернативний синтаксис (оголошений застарілим із PHP 8.1.0)

```methodsynopsis
imagepolygon(    GdImage $image,    array $points,    int $num_points,    int $color): bool
```

**imagepolygon()** створює багатокутник у зображенні `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`points`

Масив вершин багатокутника:

<table class="doctable informaltable"><tbody class="tbody"><tr><td>points[0]</td><td>= x0</td></tr><tr><td>points[1]</td><td>= y0</td></tr><tr><td>points[2]</td><td>= x1</td></tr><tr><td>points[3]</td><td>= y1</td></tr></tbody></table>

`num_points`

Загальна кількість точок (вершин) повинна бути не менше 3.

Якщо цей параметр опущено (дивіться альтернативний синтаксис), то масив `points` повинен містити парну кількість елементів і `num_points` буде обчислено як `count($points)/2`

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`num_points` оголошено застарілим. |
| 8.0.0 | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікувався коректний `gd` ресурс (Resource). |

### Приклади

**Приклад #1 Приклад використання** imagepolygon()\*\*\*\*

```php
<?php
// Создание пустого изображения
$image = imagecreatetruecolor(400, 300);

// Создание цвета полигона
$col_poly = imagecolorallocate($image, 255, 255, 255);

// Рисование многоугольника
imagepolygon($image, array(
        0,   0,
        100, 200,
        300, 200
    ),
    3,
    $col_poly);

// Вывод картинки в броузер
header('Content-type: image/png');

imagepng($image);
imagedestroy($image);
?>
```

Висновок наведеного прикладу буде схожим на:

![Висновок прикладу: imagepolygon()](images/21009b70229598c6a80eef8b45bf282b-imagepolygon.png)

### Дивіться також

-   [imagefilledpolygon()](function.imagefilledpolygon.md) \- Малювання зафарбованого багатокутника
-   [imageopenpolygon()](function.imageopenpolygon.md) \- Малює відкритий полігон
-   [imagecreate()](function.imagecreate.md) \- Створення нового палітрового зображення
-   [imagecreatetruecolor()](function.imagecreatetruecolor.md) \- Створення нового повнокольорового зображення
