Створення нового повнокольорового зображення

-   [« imagecreatefromxpm](function.imagecreatefromxpm.md)
    
-   [imagecrop »](function.imagecrop.md)
    
-   [PHP Manual](index.md)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.md)
    
-   Створення нового повнокольорового зображення
    

# imagecreatetruecolor

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

imagecreatetruecolor — створення нового повнокольорового зображення

### Опис

```methodsynopsis
imagecreatetruecolor(int $width, int $height): GdImage|false
```

**imagecreatetruecolor()** повертає об'єкт, що є чорним зображенням заданого розміру.

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
|  | У разі успішного виконання функція тепер повертає екземпляр [GDImage](class.gdimage.md); раніше повертався ресурс (resource). |

### Приклади

**Приклад #1 Створення нового потоку GD зображення та виведення зображення.**

```php
<?php
header ('Content-Type: image/png');
$im = @imagecreatetruecolor(120, 20)
      or die('Невозможно инициализировать GD поток');
$text_color = imagecolorallocate($im, 233, 14, 91);
imagestring($im, 1, 5, 5,  'Простая Текстовая Строка', $text_color);
imagepng($im);
imagedestroy($im);
?>
```

Результатом виконання цього прикладу буде щось подібне:

![Висновок прикладу: Створення нового потоку GD зображення та виведення картинки.](images/21009b70229598c6a80eef8b45bf282b-imagecreatetruecolor.png)

### Дивіться також

-   [imagedestroy()](function.imagedestroy.md) - Знищення зображення
-   [imagecreate()](function.imagecreate.md) - Створення нового палітрового зображення