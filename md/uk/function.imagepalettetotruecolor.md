Перетворює зображення на основі палітри на справжній колір

-   [« imagepalettecopy](function.imagepalettecopy.html)
    
-   [imagepng »](function.imagepng.html)
    
-   [PHP Manual](index.html)
    
-   [Функції GD та функції для роботи із зображеннями](ref.image.html)
    
-   Перетворює зображення на основі палітри на справжній колір
    

# imagepalettetotruecolor

(PHP 5> = 5.5.0, PHP 7, PHP 8)

imagepalettetotruecolor — Перетворює зображення на основі палітри на справжній колір

### Опис

```methodsynopsis
imagepalettetotruecolor(GdImage $image): bool
```

Перетворює на основі палітри зображення, створене функцією, такою як [imagecreate()](function.imagecreate.html) до справжнього (true) кольору зображення, як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Список параметрів

`image`

Об'єкт [GdImage](class.gdimage.html), що повертається однією з функцій створення зображень, наприклад, такий як [imagecreatetruecolor()](function.imagecreatetruecolor.html)

### Значення, що повертаються

Повертає **`true`**, якщо перетворення завершено, або якщо вихідне зображення вже є зображенням справжнього кольору, інакше повертається **`false`**

### список змін

| Версия | Описание                                                                                         |
|--------|--------------------------------------------------------------------------------------------------|
|        | `image` тепер чекає екземпляр [GdImage](class.gdimage.html); раніше очікували ресурс (resource). |

### Приклади

**Приклад #1 Конвертує будь-який об'єкт зображення на цей колір**

```php
<?php
// Для обратной совместимости
if(!function_exists('imagepalettetotruecolor'))
{
    function imagepalettetotruecolor(&$src)
    {
        if(imageistruecolor($src))
        {
            return(true);
        }

        $dst = imagecreatetruecolor(imagesx($src), imagesy($src));

        imagecopy($dst, $src, 0, 0, 0, 0, imagesx($src), imagesy($src));
        imagedestroy($src);

        $src = $dst;

        return(true);
    }
}

// Анонимная функция-помощник
$typeof = function() use($im)
{
    echo 'typeof($im) = ' . (imageistruecolor($im) ? 'true color' : 'palette'), PHP_EOL;
};

// Создание изображения на основе палитры
$im = imagecreate(100, 100);
$typeof();

// Преобразовать в настоящий цвет
imagepalettetotruecolor($im);
$typeof();

// Освободить память
imagedestroy($im);
?>
```

Результат виконання цього прикладу:

```
typeof($im) = palette
typeof($im) = true color
```

### Дивіться також

-   [imagecreatetruecolor()](function.imagecreatetruecolor.html) - Створення нового повнокольорового зображення
-   [imageistruecolor()](function.imageistruecolor.html) - Визначає, чи є зображення повнокольоровим