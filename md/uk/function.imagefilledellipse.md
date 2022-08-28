Малювання зафарбованого еліпса

-   [« imagefilledarc](function.imagefilledarc.html)
    
-   [imagefilledpolygon »](function.imagefilledpolygon.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Малювання зафарбованого еліпса
    

# imagefilledellipse

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagefilledellipse - Малювання зафарбованого еліпса

### Опис

```methodsynopsis
imagefilledellipse(    GdImage $image,    int $center_x,    int $center_y,    int $width,    int $height,    int $color): bool
```

Малює еліпс із центром у заданих координатах зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`center_x`

x-координат центру.

`center_y`

y-координат центру.

`width`

Ширина еліпса.

`height`

Висота еліпса.

`color`

Колір заливки. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagefilledellipse()****

```php
<?php

// создание пустого изображения
$image = imagecreatetruecolor(400, 300);

// заливка фона
$bg = imagecolorallocate($image, 0, 0, 0);

// выбор цвета для эллипса
$col_ellipse = imagecolorallocate($image, 255, 255, 255);

// рисование белого эллипса
imagefilledellipse($image, 200, 150, 300, 200, $col_ellipse);

// вывод картинки
header("Content-type: image/png");
imagepng($image);

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagefilledellipse()](images/21009b70229598c6a80eef8b45bf282b-imagefilledellipse.png)

### Примітки

> **Зауваження**
> 
> **imagefilledellipse()** ігнорує [imagesetthickness()](function.imagesetthickness.html)

### Дивіться також

-   [imageellipse()](function.imageellipse.html) - Малювання еліпса
-   [imagefilledarc()](function.imagefilledarc.html) - Малювання та заливання дуги