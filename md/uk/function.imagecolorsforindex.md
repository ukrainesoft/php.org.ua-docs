Отримання кольорів, що відповідають індексу

-   [« imagecolorset](function.imagecolorset.html)
    
-   [imagecolorstotal »](function.imagecolorstotal.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Отримання кольорів, що відповідають індексу
    

# imagecolorsforindex

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecolorsforindex — Отримання кольорів, що відповідають індексу

### Опис

```methodsynopsis
imagecolorsforindex(GdImage $image, int $color): array
```

Отримання кольорів, які відповідають заданому індексу.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`color`

Індекс кольору.

### Значення, що повертаються

Повертає асоціативний масив із червоним, зеленим, синім та альфа ключами, що містить відповідні значення для заданого індексу кольору.

### список змін

| Версия | Описание                                                                                                                                                                                         |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource).                                                                                                |
|        | Функція **imagecolorsforindex()** тепер викидає виняток [ValueError](class.valueerror.html), якщо параметр `color` поза допустимим діапазоном; раніше натомість поверталося значення **`false`** |

### Приклади

**Приклад #1 Приклад використання **imagecolorsforindex()****

```php
<?php

// открываем изображение
$im = imagecreatefrompng('nexen.png');

// получаем цвет
$start_x = 40;
$start_y = 50;
$color_index = imagecolorat($im, $start_x, $start_y);

// делаем его удобочитаемым
$color_tran = imagecolorsforindex($im, $color_index);

// что здесь ?
print_r($color_tran);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
   [red] => 226
   [green] => 222
   [blue] => 252
   [alpha] => 0
)
```

### Дивіться також

-   [imagecolorat()](function.imagecolorat.html) - Отримання індексу кольору пікселя
-   [imagecolorexact()](function.imagecolorexact.html) - Отримання індексу заданого кольору