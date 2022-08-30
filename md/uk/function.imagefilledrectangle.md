Малювання зафарбованого прямокутника

-   [« imagefilledpolygon](function.imagefilledpolygon.html)
    
-   [imagefilltoborder »](function.imagefilltoborder.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Малювання зафарбованого прямокутника
    

# imagefilledrectangle

(PHP 4, PHP 5, PHP 7, PHP 8)

imagefilledrectangle — Малювання зафарбованого прямокутника

### Опис

```methodsynopsis
imagefilledrectangle(    GdImage $image,    int $x1,    int $y1,    int $x2,    int $y2,    int $color): bool
```

Створює прямокутник, зафарбований кольором. `color` у заданому зображенні `image`. Початкова точка 1, кінцева 2. 0,0 - верхній лівий кут зображення.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`x1`

x-координат точки 1.

`y1`

y координати точки 1.

`x2`

x-координат точки 2.

`y2`

y-координата точки 2.

`color`

Колір заливки. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                          |
|--------|---------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagefilledrectangle()****

```php
<?php
// Создание изображения 55x30
$im = imagecreatetruecolor(55, 30);
$white = imagecolorallocate($im, 255, 255, 255);

// Рисование прямоугольника
imagefilledrectangle($im, 4, 4, 50, 25, $white);

// Сохранение изображения
imagepng($im, './imagefilledrectangle.png');
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefilledrectangle()](images/21009b70229598c6a80eef8b45bf282b-imagefilledrectangle.png)