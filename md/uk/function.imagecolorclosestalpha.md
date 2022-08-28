Отримання індексу кольору найближчого до заданого з урахуванням прозорості

-   [« imagecolorclosest](function.imagecolorclosest.html)
    
-   [imagecolorclosesthwb »](function.imagecolorclosesthwb.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Отримання індексу кольору найближчого до заданого з урахуванням прозорості
    

# imagecolorclosestalpha

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagecolorclosestalpha — Отримання індексу кольору найближчого до заданого з урахуванням прозорості

### Опис

```methodsynopsis
imagecolorclosestalpha(    GdImage $image,    int $red,    int $green,    int $blue,    int $alpha): int
```

Повертає індекс кольору на панелі зображення, "найближчого" до заданого RGB значення, а також `alpha` рівнем.

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

Значення в діапазоні від `0` до `127`. . `0` означає непрозорість, `127` означає абсолютну прозорість.

Параметри кольору можуть бути цілими в діапазоні від 0 до 255, або шістнадцятковими в діапазоні від 0x00 до 0xFF.

### Значення, що повертаються

Повертає індекс кольору на панелі зображення, найближчого до заданого.

### Приклади

**Приклад #1 Пошук набору кольорів зображення**

```php
<?php
// Создание изображения и преобразование его в палитровое
$im = imagecreatefrompng('figures/imagecolorclosest.png');
imagetruecolortopalette($im, false, 255);

// Цвета для поиска  (RGB)
$colors = array(
    array(254, 145, 154, 50),
    array(153, 145, 188, 127),
    array(153, 90, 145, 0),
    array(255, 137, 92, 84)
);

// Проход по каждому цвету и поиск ближайшего к нему в палитре.
// Возврат номера по порядку, RGB искомого цвета и найденное RGB соответствие
foreach($colors as $id => $rgb)
{
    $result = imagecolorclosestalpha($im, $rgb[0], $rgb[1], $rgb[2], $rgb[3]);
    $result = imagecolorsforindex($im, $result);
    $result = "({$result['red']}, {$result['green']}, {$result['blue']}, {$result['alpha']})";

    echo "#$id: Поиск ($rgb[0], $rgb[1], $rgb[2], $rgb[3]); Ближайшее сходство: $result.\n";
}

imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
#0: Поиск (254, 145, 154, 50); Ближайшее сходство: (252, 150, 148, 0).
#1: Поиск (153, 145, 188, 127); Ближайшее сходство: (148, 150, 196, 0).
#2: Поиск (153, 90, 145, 0); Ближайшее сходство: (148, 90, 156, 0).
#3: Поиск (255, 137, 92, 84); Ближайшее сходство: (252, 150, 92, 0).
```

### Дивіться також

-   [imagecolorexactalpha()](function.imagecolorexactalpha.html) - Отримання індексу заданого кольору та альфа компонента
-   [imagecolorclosest()](function.imagecolorclosest.html) - Отримання індексу кольору найближчого до заданого
-   [imagecolorclosesthwb()](function.imagecolorclosesthwb.html) - Отримання індексу кольору, що має заданий тон, білизну та затемнення