Малювання еліпса

-   [« imagedestroy](function.imagedestroy.html)
    
-   [imagefill »](function.imagefill.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Малювання еліпса
    

# imageellipse

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imageellipse - Малювання еліпса

### Опис

```methodsynopsis
imageellipse(    GdImage $image,    int $center_x,    int $center_y,    int $width,    int $height,    int $color): bool
```

Малює еліпс із центром у заданих координатах.

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

Колір еліпса. Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                          |
|--------|---------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imageellipse()****

```php
<?php

// Создание пустого изображения.
$image = imagecreatetruecolor(400, 300);

// Выбор цвета фона.
$bg = imagecolorallocate($image, 0, 0, 0);

// Закрашивание фона выбранным цветом.
imagefill($image, 0, 0, $bg);

// Выбор цвета эллипса.
$col_ellipse = imagecolorallocate($image, 255, 255, 255);

// Рисование эллипса.
imageellipse($image, 200, 150, 300, 200, $col_ellipse);

// Вывод изображения.
header("Content-type: image/png");
imagepng($image);

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imageellipse()](images/21009b70229598c6a80eef8b45bf282b-imageellipse.png)

### Примітки

> **Зауваження**
> 
> **imageellipse()** ігнорує [imagesetthickness()](function.imagesetthickness.html)

### Дивіться також

-   [imagefilledellipse()](function.imagefilledellipse.html) - Малювання зафарбованого еліпса
-   [imagearc()](function.imagearc.html) - Малювання дуги