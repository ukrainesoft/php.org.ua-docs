Малює відкритий полігон

-   [« imageloadfont](function.imageloadfont.html)
    
-   [imagepalettecopy »](function.imagepalettecopy.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Малює відкритий полігон
    

# imageopenpolygon

(PHP 7> = 7.2.0, PHP 8)

imageopenpolygon — Малює відкритий полігон

### Опис

Сигнатура починаючи з PHP 8.0.0 (не підтримується з іменованими аргументами)

```methodsynopsis
imageopenpolygon(GdImage $image, array $points, int $color): bool
```

Альтернативний синтаксис (починаючи з PHP 8.0.0)

```methodsynopsis
imageopenpolygon(    GdImage $image,    array $points,    int $num_points,    int $color): bool
```

**imageopenpolygon()** малює відкритий полігон на заданому зображенні (`image`). На відміну від [imagepolygon()](function.imagepolygon.html), лінія між останньою та першою точкою не малюється.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`points`

Масив, що містить вершини багатокутника, наприклад:

<table class="doctable informaltable"><tbody class="tbody"><tr><td>points[0]</td><td>= x0</td></tr><tr><td>points[1]</td><td>= y0</td></tr><tr><td>points[2]</td><td>= x1</td></tr><tr><td>points[3]</td><td>= y1</td></tr></tbody></table>

`num_points`

Загальна кількість точок (вершин) повинна бути не менше 3.

Якщо цей параметр опущено (дивіться альтернативний синтаксис), то масив `points` повинен містити парну кількість елементів і `num_points` буде обчислено як `count($points)/2`

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `num_points` оголошено застарілим. |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imageopenpolygon()****

```php
<?php
// Создать пустое изображение
$image = imagecreatetruecolor(400, 300);

// Выделение цвета для полигона
$col_poly = imagecolorallocate($image, 255, 255, 255);

// Нарисовать полигон
imageopenpolygon($image, array(
        0,   0,
        100, 200,
        300, 200
    ),
    3,
    $col_poly);

// Вывод изображения в браузер
header('Content-type: image/png');

imagepng($image);
imagedestroy($image);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imageopenpolygon()](images/21009b70229598c6a80eef8b45bf282b-imageopenpolygon.png)

### Дивіться також

-   [imagepolygon()](function.imagepolygon.html) - Малювання багатокутника