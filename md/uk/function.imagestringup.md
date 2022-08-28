Малювання рядка тексту вертикально

-   [« imagestring](function.imagestring.html)
    
-   [imagesx »](function.imagesx.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Малювання рядка тексту вертикально
    

# imagestringup

(PHP 4, PHP 5, PHP 7, PHP 8)

imagestringup — Малювання рядка тексту вертикально

### Опис

```methodsynopsis
imagestringup(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $string,    int $color): bool
```

Малює текст `string` вертикально на заданих координатах.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

`x`

x-координата нижнього лівого кута.

`y`

y-координата нижнього лівого кута.

`string`

Текст написи.

`color`

Ідентифікатор кольору, створений функцією [imagecolorallocate()](function.imagecolorallocate.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `font` тепер приймає як екземпляр [GdFont](class.gdfont.html), і ціле число (int); раніше приймалося лише ціле число (int). |
|  | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікувався ресурс (resource). |

### Приклади

**Приклад #1 Приклад використання **imagestringup()****

```php
<?php
// Создание изображения 100*100
$im = imagecreatetruecolor(100, 100);

// Надпись
$textcolor = imagecolorallocate($im, 0xFF, 0xFF, 0xFF);
imagestringup($im, 3, 40, 80, 'gd library', $textcolor);

// Сохранение изображения
imagepng($im, './stringup.png');
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagestringup()](images/21009b70229598c6a80eef8b45bf282b-imagestringup.png)

### Дивіться також

-   [imagestring()](function.imagestring.html) - Малювання рядка тексту горизонтально
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту