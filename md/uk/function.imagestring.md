Малювання рядка тексту горизонтально

-   [« imagesettile](function.imagesettile.html)
    
-   [imagestringup »](function.imagestringup.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Малювання рядка тексту горизонтально
    

# imagestring

(PHP 4, PHP 5, PHP 7, PHP 8)

imagestring — Малювання рядка тексту горизонтально

### Опис

```methodsynopsis
imagestring(    GdImage $image,    GdFont|int $font,    int $x,    int $y,    string $string,    int $color): bool
```

Малює текст `string` на заданих координатах.

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

`font`

Може приймати значення 1, 2, 3, 4, 5 для вбудованих шрифтів у кодуванні latin2 (вища кількість відповідає більшому шрифту) або екземпляр [GdFont](class.gdfont.html), що повертається функцією [imageloadfont()](function.imageloadfont.html)

`x`

x-координата верхнього лівого кута.

`y`

y-координата верхнього лівого кута.

`string`

Рядок тексту.

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

**Приклад #1 Приклад використання **imagestring()****

```php
<?php
// Создание изображения 100*30
$im = imagecreate(100, 30);

// Белый фон, синий текст
$bg = imagecolorallocate($im, 255, 255, 255);
$textcolor = imagecolorallocate($im, 0, 0, 255);

// Надпись в левом верхнем углу
imagestring($im, 5, 0, 0, 'Hello world!', $textcolor);

// Вывод изображения
header('Content-type: image/png');

imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: imagestring()](images/21009b70229598c6a80eef8b45bf282b-imagestring.png)

### Дивіться також

-   [imagestringup()](function.imagestringup.html) - Малювання рядка тексту вертикально
-   [imageloadfont()](function.imageloadfont.html) - Завантаження шрифту
-   [imagettftext()](function.imagettftext.html) - Малювання тексту на зображенні шрифтом TrueType