Створення нового палітрового зображення

-   [« imagecopyresized](function.imagecopyresized.html)
    
-   [imagecreatefromavif »](function.imagecreatefromavif.html)
    
-   [PHP Manual](index.html)
    
-   [Функции GD и функции для работы с изображениями](ref.image.html)
    
-   Створення нового палітрового зображення
    

# imagecreate

(PHP 4, PHP 5, PHP 7, PHP 8)

imagecreate - Створення нового палітрового зображення

### Опис

```methodsynopsis
imagecreate(int $width, int $height): GdImage|false
```

**imagecreate()** повертає ідентифікатор зображення, що представляє собою порожнє зображення заданого розміру.

Ми рекомендуємо використовувати функцію [imagecreatetruecolor()](function.imagecreatetruecolor.html) замість **imagecreate()**, так як вона обробляє зображення з максимально можливою якістю. Якщо потрібно вивести палітру зображення, то [imagetruecolortopalette()](function.imagetruecolortopalette.html) необхідно викликати безпосередньо перед збереженням зображення за допомогою [imagepng()](function.imagepng.html) або [imagegif()](function.imagegif.html)

### Список параметрів

`width`

Ширина зображення.

`height`

Висота зображення.

### Значення, що повертаються

Повертає об'єкт зображення у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.html); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Створення нового потоку GD зображення та виведення зображення.**

```php
<?php
header("Content-Type: image/png");
$im = @imagecreate(110, 20)
    or die("Невозможно создать поток изображения");
$background_color = imagecolorallocate($im, 0, 0, 0);
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  "A Simple Text String", $text_color);
imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Створення нового GD потоку зображення та виведення зображення.](images/21009b70229598c6a80eef8b45bf282b-imagecreate.png)

### Дивіться також

-   [imagedestroy()](function.imagedestroy.html) - Знищення зображення
-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення