---
navigation:
  - function.imagecolorallocate.html: « imagecolorallocate
  - function.imagecolorat.html: imagecolorat »
  - index.html: PHP Manual
  - ref.image.html: Функції GD та функції для роботи із зображеннями
title: imagecolorallocatealpha
---
# imagecolorallocatealpha

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

imagecolorallocatealpha — Створення кольору для зображення

### Опис

```methodsynopsis
imagecolorallocatealpha(    GdImage $image,    int $red,    int $green,    int $blue,    int $alpha): int|false
```

**imagecolorallocatealpha()** працює аналогічно до функцій [imagecolorallocate()](function.imagecolorallocate.html), але ще додає до кольору параметр `alpha`, що відповідає за прозорість.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`red`

Значення червоного компонента кольору.

`green`

Значення зеленого компонента кольору.

`blue`

Значення синього компонента кольору.

`alpha`

Значення в діапазоні від `0` до `127`. . `0` означає непрозорий колір, `127` означає повну прозорість.

Параметри `red` `green` і `blue` можуть бути цілими в діапазоні від 0 до 255 або шістнадцятковими в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Ідентифікатор кольору або **`false`** у разі виникнення помилки під час створення кольору.

**Увага**

Ця функція може повертати як логічне значення \*\*`false`\*\*так і значення не типу boolean, яке наводиться до **`false`**. За більш детальною інформацією зверніться до розділу [Булев тип](language.types.boolean.html). Використовуйте [оператор ===](language.operators.comparison.html) для перевірки значення, яке повертається цією функцією.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecolorallocatealpha()****

```php
<?php
$size = 300;
$image=imagecreatetruecolor($size, $size);

// создадим белый фон с чёрной рамкой
$back = imagecolorallocate($image, 255, 255, 255);
$border = imagecolorallocate($image, 0, 0, 0);
imagefilledrectangle($image, 0, 0, $size - 1, $size - 1, $back);
imagerectangle($image, 0, 0, $size - 1, $size - 1, $border);

$yellow_x = 100;
$yellow_y = 75;
$red_x    = 120;
$red_y    = 165;
$blue_x   = 187;
$blue_y   = 125;
$radius   = 150;

// создание цветов с альфа компонентом
$yellow = imagecolorallocatealpha($image, 255, 255, 0, 75);
$red    = imagecolorallocatealpha($image, 255, 0, 0, 75);
$blue   = imagecolorallocatealpha($image, 0, 0, 255, 75);

// рисование 3-х пересекающихся окружностей
imagefilledellipse($image, $yellow_x, $yellow_y, $radius, $radius, $yellow);
imagefilledellipse($image, $red_x, $red_y, $radius, $radius, $red);
imagefilledellipse($image, $blue_x, $blue_y, $radius, $radius, $blue);

// не забудьте вывести правильный заголовок!
header('Content-Type: image/png');

// и наконец, вывод
imagepng($image);
imagedestroy($image);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Приклад використання imagecolorallocatealpha()](images/21009b70229598c6a80eef8b45bf282b-imagecolorallocatealpha.png)

**Приклад #2 Перетворення типових альфа-значень для використання з **imagecolorallocatealpha()****

Зазвичай альфа-значення `0` позначають повністю прозорі пікселі, а альфа-канал має 8 бітів. Щоб перетворити такі альфа-значення для сумісності з **imagecolorallocatealpha()**, досить трохи простої арифметики:

```php
<?php
$alpha8 = 0; // полностью прозрачный
var_dump(127 - ($alpha8 >> 1));
$alpha8 = 255; // полностью непрозрачный
var_dump(127 - ($alpha8 >> 1));
?>
```

Результат виконання цього прикладу:

```
int(127)
int(0)
```

### Дивіться також

-   [imagecolorallocate()](function.imagecolorallocate.html) - Створення кольору для зображення
-   [imagecolordeallocate()](function.imagecolordeallocate.html) - Розрив асоціації змінної із кольором для заданого зображення
