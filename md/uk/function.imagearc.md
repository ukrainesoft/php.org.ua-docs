Малювання дуги

-   [« imageantialias](function.imageantialias.html)
    
-   [imageavif »](function.imageavif.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Малювання дуги
    

# imagearc

(PHP 4, PHP 5, PHP 7, PHP 8)

imagearc - Малювання дуги

### Опис

```methodsynopsis
imagearc(    GdImage $image,    int $center_x,    int $center_y,    int $width,    int $height,    int $start_angle,    int $end_angle,    int $color): bool
```

**imagearc()** малює дугу кола із заданими координатами центру.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`center_x`

x-координат центру.

`center_y`

y-координат центру.

`width`

Ширина дуги.

`height`

Висота дуги.

`start_angle`

Кут початку дуги у градусах.

`end_angle`

Кут закінчення дуги у градусах. 0° відповідає положенню 3 години, дуга малюється за годинниковою стрілкою.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Малювання кола за допомогою функції **imagearc()****

```php
<?php

// создаём изображение 200*200
$img = imagecreatetruecolor(200, 200);

// создаём несколько цветов
$white = imagecolorallocate($img, 255, 255, 255);
$red   = imagecolorallocate($img, 255,   0,   0);
$green = imagecolorallocate($img,   0, 255,   0);
$blue  = imagecolorallocate($img,   0,   0, 255);

// рисуем голову
imagearc($img, 100, 100, 200, 200,  0, 360, $white);
// рот
imagearc($img, 100, 100, 150, 150, 25, 155, $red);
// глаза
imagearc($img,  60,  75,  50,  50,  0, 360, $green);
imagearc($img, 140,  75,  50,  50,  0, 360, $blue);

// выводим изображение в браузере
header("Content-type: image/png");
imagepng($img);

// освобождаем память
imagedestroy($img);

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Малювання кола за допомогою функції imagearc()](images/21009b70229598c6a80eef8b45bf282b-imagearc.png)

### Дивіться також

-   [imagefilledarc()](function.imagefilledarc.html) - Малювання та заливання дуги
-   [imageellipse()](function.imageellipse.html) - Малювання еліпса
-   [imagefilledellipse()](function.imagefilledellipse.html) - Малювання зафарбованого еліпса