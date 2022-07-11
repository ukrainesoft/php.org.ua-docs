- [«imagesetinterpolation](function.imagesetinterpolation.md)
- [imagesetstyle »](function.imagesetstyle.md)

- [PHP Manual](index.md)
- [Функції GD та функції для роботи із зображеннями](ref.image.md)
- Малювання точки

#imagesetpixel

(PHP 4, PHP 5, PHP 7, PHP 8)

imagesetpixel — Малювання точки

### Опис

**imagesetpixel**(
[GdImage](class.gdimage.md) `$image`,
int `$x`,
int `$y`,
int `$color`
): bool

**imagesetpixel()** малює точку (піксел) на заданих координатах.

### Список параметрів

`image`
Об'єкт [GdImage](class.gdimage.md), який повертається однією з функцій
створення зображень, наприклад, такий як
[imagecreatetruecolor()](function.imagecreatetruecolor.md).

`x`
x-координат.

`y`
y-координат.

`col`
Ідентифікатор кольору, створений функцією
[imagecolorallocate()](function.imagecolorallocate.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                         |
|--------|----------------------------------------------------------------------------------------------|
| 8.0.0  | image тепер чекає екземпляр [GdImage](class.gdimage.md); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagesetpixel()****

Малювання "випадкових" точок, що дає в результаті фрактальне
зображення.

` <?php$x = 200;$y = 200;$gd = imagecreatetruecolor($x, $y);$corners[0] = array('x' => 100, 'y' =>  10); corners[1] = array('x' =>   0, 'y' => 190);$corners[2] = array('x' => 200, 'y' => 190);$red = image $gd, 255, 0, 0);for ($i = 0; $i < 100000; $i++) { imagesetpixel($gd, round($x),round($y), $red); $a==rand(0,2); $x = ($x + $corners[$a]['x']) / 2; $y = ($y + $corners[$a]['y']) / 2;}header('Content-Type: image/png');imagepng($gd);?> `

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу:
imagesetpixel()](images/21009b70229598c6a80eef8b45bf282b-imagesetpixel.png)

### Дивіться також

- [imagecreatetruecolor()](function.imagecreatetruecolor.md) -
Створення нового повнокольорового зображення
- [imagecolorallocate()](function.imagecolorallocate.md) - Створення
кольори для зображення
- [imagecolorat()](function.imagecolorat.md) - Отримання індексу
кольору пікселя
