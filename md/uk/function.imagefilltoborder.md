Заливка кольором

-   [« imagefilledrectangle](function.imagefilledrectangle.md)
    
-   [imagefilter »](function.imagefilter.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Заливка кольором
    

# imagefilltoborder

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefilltoborder - Заливка кольором

### Опис

```methodsynopsis
imagefilltoborder(    GdImage $image,    int $x,    int $y,    int $border_color,    int $color): bool
```

**imagefilltoborder()** робить заливку області, обмеженою кольором `border_color`. Початкова координата `x` `y` (лівий верхній кут має координати 0, 0), а область зафарбовується кольором `color`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.md), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.md)

`x`

x-координата початку.

`y`

y-координата початку.

`border_color`

Колір заливання кордону. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

`color`

Колір заливки. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Забарвлення еліпса**

```php
<?php
// создание изображения, установка белого фона
$im = imagecreatetruecolor(100, 100);
imagefilledrectangle($im, 0, 0, 100, 100, imagecolorallocate($im, 255, 255, 255));

// рисование эллипса закрашенного черным цветом
imageellipse($im, 50, 50, 50, 50, imagecolorallocate($im, 0, 0, 0));

// установка цвета границы заливки
$border = imagecolorallocate($im, 0, 0, 0);
$fill = imagecolorallocate($im, 255, 0, 0);

// заливка области
imagefilltoborder($im, 50, 50, $border, $fill);

// вывод и освобождение памяти
header('Content-type: image/png');
imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Забарвлення еліпса](images/21009b70229598c6a80eef8b45bf282b-imagefilltoborder.png)

### Примітки

Алгоритм не запам'ятовує явно, які пікселі вже були встановлені, а швидше робить висновок за кольором пікселя, тому він не може відрізнити щойно встановлені пікселі від пікселів, які вже є. Це означає, що вибір будь-якого кольору заливки, який вже використовується у зображенні, може призвести до небажаних результатів.