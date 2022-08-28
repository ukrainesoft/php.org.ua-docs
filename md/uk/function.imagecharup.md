Малювання символу вертикально

-   [« imagechar](function.imagechar.html)
    
-   [imagecolorallocate »](function.imagecolorallocate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Малювання символу вертикально
    

# imagecharup

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecharup — Малювання символу вертикально

### Опис

```methodsynopsis
imagecharup(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $char,    int $color): bool
```

Малює символ `char` вертикально на заданих координатах зображення `image`

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

`x`

x-координата початку малювання.

`y`

y-координата початку малювання.

`char`

Символ для малювання.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `font` тепер приймає як екземпляр [GdFont](class.gdfont.html), і ціле число (int); раніше приймалося лише ціле число (int). |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagecharup()****

```php
<?php

$im = imagecreate(100, 100);

$string = 'Надо учитывать, что первый символ в строке — N';

$bg = imagecolorallocate($im, 255, 255, 255);
$black = imagecolorallocate($im, 0, 0, 0);

// печатает чёрный символ "Z" на белом фоне
imagecharup($im, 3, 10, 10, $string, $black);

header('Content-type: image/png');
imagepng($im);

?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagecharup()](images/21009b70229598c6a80eef8b45bf282b-imagecharup.png)

### Дивіться також

-   [imagechar()](function.imagechar.html) - Малювання символу по горизонталі
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту